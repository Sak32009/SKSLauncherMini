# Changelog

## v2.0.2

- Fixed https://github.com/otavepto/gbe_fork/issues/64
- Fixed an issue with appids that don't have achievements.
- Now depots.txt only contains the ids of the depots that are for Windows os.
  Set "Retriever->RetrieveDLC" to "true" to get a complete list.
- Now while the notification is shown the notification sound is played.
  Previously the notification sound would only play after the notification was shown.
- Added "Experimental->ip_country", "Experimental->disable_overlay_warning_any", "Experimental->disable_overlay_warning_bad_appid", "Experimental->disable_overlay_warning_forced_setting", "Experimental->disable_overlay_warning_local_save", "Experimental->download_steamhttp_requests" and "Experimental->force_steamhttp_success" settings.
- Removed "Experimental->disable_overlay_warning" and "Experimental->http_online" settings.

## v2.0.1

- "Generator->AchievementsImages" setting renamed to "Generator->AchievementImages"
- Added "Experimental->crash_printer_location" setting.

## v2.0.0

- The name has been changed to SKSLauncherMini.

Almost all changes:

- https://cs.rin.ru/forum/viewtopic.php?p=2946780#p2946780
- https://cs.rin.ru/forum/viewtopic.php?p=2951241#p2951241
- https://cs.rin.ru/forum/viewtopic.php?p=2973039#p2973039
- https://cs.rin.ru/forum/viewtopic.php?p=2976532#p2976532

# Changelog SteamLauncherMini

## v1.1.8

- Changed the description usage of "SteamCloud". Now you can choose whether to backup all game saves or just a single game and you can also restore them directly from ludusavi.

## v1.1.7.2

- "Cloud->Enabled" is now disabled by default.

## v1.1.7.1

- Fixed an issue introduced in v1.1.7.

## v1.1.7

- Fixed "Launcher->Target", "Launcher->StartIn", "Launcher->SteamClientPath", "Launcher->SteamClientPath64", "Cloud->Path".

## v1.1.6.3 | TEST VERSION

- Now SteamLauncherMini.json is generated correctly, the "CommandsLine" entry is "CommandLine".

## v1.1.6.2 | TEST VERSION

- Fixed the game name in "SteamLauncherMini/AchievementsWatcher/GAME_ID/view.html".

## v1.1.6.1 | TEST VERSION

SteamLauncherMini:

- To watch the achievements and their progress, since the SteamLauncherMini doesn't have an interface, when starting the launcher a static HTML page is generated in the path "SteamLauncherMini/AchievementsWatcher/GAME_ID/view.html". If you haven't unlocked any achievements, "view.html" will be deleted. Here is an example of the content: https://i.imgur.com/M4HSgnJ.png
- Fixed an issue with AchievementsWatcher not notifying unlocked achievement in some cases.
- Fixed an issue with setting the environments (SteamAppId, SteamGameId) at game launch.
- Fixed an issue with the steamclient.dll and steamclient64.dll paths in the Steam registry.

SteamRetriever:

- Now when generating the acf, the "LastOwner" value will be equal to the SteamID of the logged in account.
- Now if SaveCredentials is deactivated, you will be asked if you want to delete the data previously saved.

## v1.1.6

SteamLauncherMini:

- New settings: "AchievementsWatcher->Enabled", "AchievementsWatcher->AppId".
- The minimum os required now is Windows 10.

SteamRetriever:

- Minor fixes.

## v1.1.5

- Fixed "Launcher->InjectDll" on x32 os.
- Removed "Generator->Refresh", now just delete the folder "SteamLauncherMini/GAME_ID" and automatically the data will be refreshed.
- Now the setting "Generator->DLCUnknowns" in addition to "SteamRetriever Unknown App" also skips the dlc names starting with "SteamDB Unknown App" (in case you have a custom dlcs list).

## v1.1.4

- Fixed appids with type "beta".

## v1.1.3

SteamLauncherMini, SteamRetriever, SteamACFGenerator:
A big problem with Python is distribution. What further i managed to do is:

- SteamLauncherMini reduced by about 5mb (in total it has been reduced by about 10mb since version 1.1.1).
- SteamRetriever and SteamACFGenerator reduced by about 2mb.

Better than node.js, 2 lines of code equals 40mb of executable.

Also:

- Fixed a bug with login when wrong password was entered.
- Fixed a bug with getting controller config information.
- Fixed a bug that generated empty files.
- Changed the logic for clearing the logs and as a result the startup is much faster.

SteamLauncherMini:

- Ludusavi is now no longer bundled with SteamLauncherMini. The "Settings->Cloud" setting has been removed and two new settings "Cloud->Enabled" and "Cloud->Path" have been introduced.

## v1.1.2

SteamLauncherMini:

- Reduced the app size by about 4mb.

SteamRetriever:

- Fixed appids without public manifests.
- Fixed appids with type "application" (fixed launching "Wallpaper Engine").

## v1.1.1

SteamRetriever:

- Added "--no-retrieve-dlcs" command.
- Added shorthand command lines.
- Renamed "--download-acf" to "--generate-acf", "--download-all" to "--retrieve-all", "--download-images" to "--retrieve-images", "--download-achievements" to "--retrieve-achievements", "--download-inventory" to "--retrieve-inventory", "--download-controller" to "--retrieve-controller".
- Removed GUI for inputs and windows.
- Fixed "--save-credentials" command.
- Fixed an issue where if i added a new feature to SteamLauncherMini, it made the executable heavy even if SteamRetriever didn't use those features.

SteamLauncherMini:

- Fixed issue with multiple instances.
- Fixed an issue where it took 10 seconds or more to launch the game.

## v1.1.0

- Fixed starting with games that are not released on steam (Saints Row 2022).
- Updated Ludusavi to v0.15.2.

## v1.0.9

- Fixed SteamRetriever "No such file or directory".

## v1.0.8

- New settings: DLC, Generator->DLCUnknowns
- SteamRetriever now also finds unknown dlcs.

## v1.0.7

- The big change in this release is that SmartSteamLoader has been removed and i've recreated its functions purely in python.
- Renamed settings: SteamClient->ApiKey to SteamClient->WebApiKey and SteamClient->AskCredentials to SteamClient->SaveCredentials.
- Fixed login.
- Improved caching logic.
- And others...

## v1.0.6

- Now the username and password are no longer in the configuration file but are saved in the "Windows Credential Locker".
- New settings: Settings->Cloud, SteamClient->AskCredentials, SteamClient->ApiKey, Generator->AchievementsImages
- Now the configuration file is a json.
- SteamRetriever is standalone.
- Updated Ludusavi to v0.15.1, thanks to Ludusavi improvements it is now no longer necessary to extract the game name from pcgamingwiki.
- Faster than the old versions.
- And more...

## v1.0.5

- I've done something wrong.

## v1.0.4

- "SteamCloud" now searches by game_appid, game_name and pcgamingwiki_name
- General improvements.

## v1.0.0.3

- I forgot DisableLanOnly.

## v1.0.0.2

- Fixed controller.
- Fixed achievements.
- Logical improvements.

## v1.0.0.1

- Added "SteamCloud".
- Fixed an issue with the generation of achievements on every launch.

## v1.0.0.0

- Initial release.
