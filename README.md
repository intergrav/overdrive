# Overdrive

Overdrive is a (small) client-side modpack that can be used as a base for profiles that improves the games performance while minimally modifying the game's visuals and functionality. Updated frequently. Licensed under the Unlicense. For suggestions, create issues/pull requests on the [Git repository](https://github.com/intergrav/overdrive).

## Mod information

Most of these config changes were designed for the vanilla game, so if you are playing on things like large modded moons, then you may want to tweak some settings. This section will show you what you may want to change.

- **CullFactory** stops rendering rooms and objects that are not supposed to be visible to the user, which heavily improves the performance inside the factory. Other than it's defaults, this mod is configured to:
    - Enabled distance culling. In-factory cull distance is set to 60. Surface cull distance is set to 200.
        - *Playing on modded moons? If they are large, you may want to increase the **surface** cull distance to ~`300`-`400`. This will let you see further on moons at the cost of performance. [Some mods could override this](https://thunderstore.io/c/lethal-company/p/sfDesat/ViewExtension/).*
        - *Inside the factory and notice rooms in the distance disappearing at all? You may want to increase the **factory** cull distance to `80` or higher at the cost of performance. The higher this value is, the laggier the game might be.*
- **LC Symphony** speeds up startup by skipping screens, such as the online/local startup screen and terminal boot animation. Other than it's defaults, this mod is also configured to:
    - Disable the ping indicator that this mod adds to maintain vanilla parity. You can re-enable in config if you want a ping indicator.
- **HD Lethal Company** adds extra graphics settings. This modpack tries to change these settings without affecting the appearance noticeably to most people. This mod is configured to:
    - Reduce texture quality since the game's resolution is already very low.
        - *Are UI elements appearing blurry at all? Some UI elements from mods may become blurry due to this setting, and if so, you can set it back to the original value at a cost of performance.*
    - Fog quality is set to very low (not off) as volumetric fog can be very heavy on some systems.
    - Reduces the LODs since the game is usually foggy and so it won't be noticable to most.
        - *If you have a mod that increases the view distance or you remove fog, you may want to set the LODs back to it's original value. I only have it set low because it's already hard to see far in the vanilla game. For more information about LODs in computer graphics, [look here](https://en.wikipedia.org/wiki/Level_of_detail_(computer_graphics)).*
    - Shadowmap resolution is reduced from `2048` to `256` because the game resolution is already low.
    - Resolution is kept as game default `520p`/`1.000`.
- **DissonanceLagFix** significantly reduces lag spikes by changing the log level of DissonanceVoip. When a lag spike would occur, Dissonance previously spammed tons of warnings into the log, which extended the duration of the lag spike.
- **FixRPCLag** sets the NetworkManager log level to `Normal`. Previously it was set to `Developer` which made every RPC error print out the RPC table contents, causing a huge lag spike that can last several seconds.

## Looking for more speed?

Are you on a very low end device looking to improve the game performance even more, **even if it affects appearance?** Here are some things you can try, per mod:

- In **HDLethalCompany**, you can try lowering the graphics more than this modpack does.
    - If you are on a very low end device, you can disable fog which will heavily improve performance. 
        - *Keep in mind that this is basically cheating as this allows you to fully see in the distance without issue. Only do this if you really need to.*
    - Disable shadows by setting shadow quality to `0`. Shadows can be decently heavy in some cases.
    - Disable post processing, which will change the game's look but can improve performance.
    - Lower the game's resolution scale multiplier, which will improve performance.
        - *Not recommended because this can make it very hard to see what's happening in-game at low resolutions.*
    - Disable foliage, which will prevent the game from rendering bushes/grass.
    - Lower texture resolution to `1` or `0`. This isn't guaranteed to improve performance but it might help on some machines.
- In **CullFactory**, there are various settings to tweak.
    - At the cost of render distance, a.k.a. being able to see far, you can decrease the cull distance which will make the game render less stuff.
    - Try looking through it's config for some other settings that you may want to mess around with.
- You could try disabling **BepInEx** logging, which will make it very hard to solve issues if you have any, but may possibly improve performance slightly on some systems.

## Changelog

You could possibly experience issues on Lethal Company versions that the modpack isn't yet tested for, however it's very rare. Version numbers will appear here as "Modpack Version - Tested LC Version".

### 1.2.0 - LC49

- Update CullFactory from 0.8.3 to 0.8.5
- Add FixRPCLag
- Add DissonanceLagFix
- Add information to README

### 1.1.4 - LC49

- Add more information to README
- Shorten description in manifest

### 1.1.3 - LC49

- Shorten description in manifest

### 1.1.2 - LC49

- Fix README consistency

### 1.1.1 - LC49

- Heavily improve README with more information
- Improve icon

### 1.1.0 - LC49

- Remove Frosty's Fastest Company. Doesn't seem to do much and from a rough benchmark I tend to get slightly better framerate without it. May also possibly conflict with other mods in this modpack from a quick look through it's decompiled source code
- Improve README a little bit

### 1.0.1 - LC49

- Increased Cull Factory in-factory cull distance to 60 to make the culling less noticable in the factories
- Show tested Lethal Company version in the manifest description
- Make the icon look better

### 1.0.0 - LC49

- Very open for improvement - create issues/pull requests on the [GitHub](https://github.com/intergrav/overdrive) repository