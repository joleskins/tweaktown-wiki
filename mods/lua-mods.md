# Lua mods

**This is a nerd section and it's assumed that you know how to use Lua, and know how Etterna theming works. This is -not- documentation for etterna lua itself, just how this specific feature works.**



tweaktown loads lua mods from `tweaktown/Mods` as plug 'n play modules that can easily be shared instead of editing the theme's own lua files.



When making mods, you can use screen names in the code to decide where something shows up. If you don't specify screens for loading/showing specific things, they'll show up everywhere. You can also include things for multiple, cherry picked screens because of this.



The screen name is given through `LoadActorWithParams` as `Var("screenName")`.

So you can grab the screenName param like this:

```
local screenName = Var("screenName") or ""
```



**Screen names**

```
"IntroScreen"
"MainMenu"
"OptionMenu"
"PackDownloader"
"SongSelect"
"ProfileSelect"
"AssetSelect"
"Gameplay"
"Results"
"LoadingMenu"
"PromptOverlay"
```

These are manually defined screen names and not what the StepMania engine uses internally. Below is a translation between the two

```
"IntroScreen" = "ScreenInit2" (ScreenInit is only shown for theme preferences prompt)
"MainMenu" = "ScreenTitleMenu"
"OptionMenu" = "ScreenOptionsService" (and all its children) + "ScreenPlayerOptions"
"PackDownloader" = "ScreenPackDownloader"
"SongSelect" = "ScreenSelectMusic
"ProfileSelect" = "ScreenSelectProfile"
"AssetSelect" = "ScreenAssetSettings"
"Gameplay" = "ScreenGameplay"
"Results" = "ScreenEvaluationNormal"
"LoadingMenu" = "ScreenProfileLoad" + "ScreenProfileSave"
"PromptOverlay" = "ScreenPrompt"
```



**Standalone files**

Individual .lua files with any given name in the Mods folder will be loaded. These can have basically any name you want



**Folders**

If your mod is more advanced or requires images/videos/etc., you can include the mod as a folder in the Mods folder. Just remember to include a "default.lua" file inside your own mod folder.
