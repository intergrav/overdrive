# Overdrive

Overdrive is a (small) client-side modpack that can be used as a base for profiles that improves the games performance while minimally modifying the game's visuals and functionality. Updated frequently. Licensed under the Unlicense.

For suggestions, create issues/pull requests on the [GitHub](https://github.com/intergrav/overdrive) repository. I'm pretty new to this, so there could be some oversights.

## Mod information

- **CullFactory** stops rendering rooms and objects that are not supposed to be visible to the user, which heavily improves the performance inside the factory. This modpack also enables a setting for the culling range, with the mod's defaults.
- **LC Symphony** speeds up startup. This modpack sets the `LaunchOption` setting to `online` so that the game automatically chooses online on startup, and also is set to skip the terminal boot screen. The ping metric is disabled to maintain parity with the Vanilla game, but you can enable it in the config.
- **HD Lethal Company** is configured to:
    - Reduce texture quality since the game's resolution is already low
    - Fog quality is set to very low (not off) as volumetric fog can be very heavy on some systems
    - Reduces the LODs since the game is usually very foggy and it won't be noticable to most
        - *If you have a mod that increases the view distance or removes fog, you may want to set the LODs back to the original value. I only have it set low because it's already hard to see in the distance in the Vanilla game.*
    - Shadowmap resolution is reduced to `256` because the game resolution is already low
    - Resolution is kept as game default `520p`/`1.000`

## Changelog

You could possibly experience issues on Lethal Company versions that the modpack isn't yet tested for, however it's rare. Version numbers will appear here as "Modpack Version - Tested LC Version".

### 1.0.1 - LC49

- Increased Cull Factory in-factory cull distance to 60 to make the culling less noticable in the factories
- Show tested Lethal Company version in the manifest description
- Make the icon look better

### 1.0.0 - LC49

Very open for improvement - create issues/pull requests on the [GitHub](https://github.com/intergrav/overdrive) repository