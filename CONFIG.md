# Config

## LAUNCHER

### Launcher -> AppId [type: number] [required]

> NO_DESCRIPTION

#### EXAMPLES:

`534380`

### Launcher -> Target [type: string] [required]

> NO_DESCRIPTION

#### EXAMPLES:

`DyingLightGame_x64_rwdi.exe`

`D:/Games/DyingLight2StayHuman/ph/work/bin/x64/DyingLightGame_x64_rwdi.exe`

### Launcher -> StartIn [type: string] [default: ./]

> NO_DESCRIPTION

#### EXAMPLES:

`D:/Games/DyingLight2StayHuman/ph/work/bin/x64`

### Launcher -> CommandLine [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`-nologos`

### Launcher -> SteamApiPath [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`steam_api64.dll`

`../../../../engine/source/bin/x64/steam_api64.dll`

### Launcher -> SteamClientPath [type: string] [required]

> NO_DESCRIPTION

#### EXAMPLES:

`steamclient.dll`

`D:/Goldberg/steamclient.dll`

### Launcher -> SteamClientPath64 [type: string] [required]

> NO_DESCRIPTION

#### EXAMPLES:

`steamclient64.dll`

`D:/Goldberg/steamclient64.dll`

### Launcher -> Persist [type: bool] [default: false]

> NO_DESCRIPTION

### Launcher -> InjectDll [type: bool] [default: false]

> NO_DESCRIPTION

### Launcher -> ParanoidMode [type: bool] [default: false]

> NO_DESCRIPTION

## RETRIEVER

### Retriever -> LoginSave [type: bool] [default: true]

> NO_DESCRIPTION

### Retriever -> LoginAnonymous [type: bool] [default: false]

> NO_DESCRIPTION

### Retriever -> TopOwners [type: array] [default: []]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"TopOwners": [
  76561198028121353,
  76561197993544755
]
```

### Retriever -> RetrieveDLC [type: bool] [default: false]

> NO_DESCRIPTION

## SETTINGS

### Settings -> Offline [type: bool] [default: false]

> NO_DESCRIPTION

### Settings -> DisableLobbyCreation [type: bool] [default: false]

> NO_DESCRIPTION

### Settings-> DisableNetworking [type: bool] [default: false]

> NO_DESCRIPTION

### Settings -> DisableOverlay [type: bool] [default: false]

> NO_DESCRIPTION

### Settings -> DisableLanOnly [type: bool] [default: false]

> NO_DESCRIPTION

### Settings -> ListenPort [type: number] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`47584`

## ACCOUNT

### WARNING: This options creates the force\_\*.txt files, it does not change the global settings.

### Account -> Name [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`Sak32009`

### Account -> SteamId [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`76561198014932880`

### Account -> Language [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`english`

## CLOUD

### Cloud -> Enabled [type: bool] [default: false]

> NO_DESCRIPTION

### Cloud -> Path [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`ludusavi.exe`

`D:/Ludusavi/ludusavi.exe`

## ACHIEVEMENTS

### Achievements -> Enabled [type: bool] [default: true]

> NO_DESCRIPTION

### Achievements -> Sound [type: bool] [default: true]

> NO_DESCRIPTION

### Achievements -> Shortcut [type: string] [default: alt+s]

> NO_DESCRIPTION

#### EXAMPLES:

`ctrl+alt+s`

### Achievements -> CustomPath [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`C:/Users/Public/Documents/EMPRESS`

## GENERATOR

### Generator -> DLC [type: bool] [default: true]

> NO_DESCRIPTION

### Generator -> DLCUnknowns [type: bool] [default: true]

> NO_DESCRIPTION

### Generator -> AchievementImages [type: bool] [default: true]

> NO_DESCRIPTION

### Generator -> AchievementsAndStats [type: bool] [default: true]

> NO_DESCRIPTION

### Generator -> Inventory [type: bool] [default: true]

> NO_DESCRIPTION

### Generator -> Controller [type: bool] [default: true]

> NO_DESCRIPTION

## DLC [type: object | bool] [default: {}]

> NO_DESCRIPTION

#### EXAMPLES:

> If you want to unlock only the DLC in the list:

```json
"DLC": {
  "1937531": "Dying Light 2 - Ultimate Upgrade"
}
```

> If you want to unlock all DLC:

```json
"DLC": true
```

## HTTP [type: object] [default: {}]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"HTTP":{
  "https://accounts.starbreeze.com/iam/oauth/token": "{\"access_token\":\"aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa\",\"bans\":null,\"display_name\":\"\",\"expires_in\":3600,\"is_comply\":true,\"jflgs\":0,\"namespace\":\"PD2\",\"namespace_roles\":null,\"permissions\":[],\"platform_id\":\"\",\"platform_user_id\":\"\",\"roles\":null,\"scope\":\"account commerce social publishing analytics\",\"token_type\":\"Bearer\",\"user_id\":\"\",\"xuid\":\"\"}"
}
```

## AppPaths [type: object] [default: {}]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"AppPaths": {
  "556760": "../DLCRoot0"
}
```

## CustomBroadcasts [type: array] [default: []]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"CustomBroadcasts":[
  "192.168.3.255"
  "removethis.test.domain.com"
]
```

## Leaderboards [type: array] [default: []]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"Leaderboards": [
  "LEADERBOARDTEST=0=0"
]
```

## SubscribedGroups [type: array] [default: []]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"SubscribedGroups": [
  103582791433980119
]
```

## EXPERIMENTAL

### Experimental -> force_branch_name [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`beta`

### Experimental -> crash_printer_location [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`./path/relative/to/dll/crashes.txt`

### Experimental -> ip_country [type: string] [default: empty]

> NO_DESCRIPTION

#### EXAMPLES:

`US`

### Experimental -> achievements_bypass [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_account_avatar [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_overlay_achievement_notification [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_overlay_friend_notification [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_overlay_warning_any [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_overlay_warning_bad_appid [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_overlay_warning_forced_setting [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_overlay_warning_local_save [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> disable_source_query [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> download_steamhttp_requests [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> force_steamhttp_success [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> steam_deck [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> gc_token [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> is_beta_branch [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> new_app_ticket [type: bool] [default: false]

> NO_DESCRIPTION

### Experimental -> installed_app_ids [type: array] [default: []]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"installed_app_ids": [
  "570",
  "534380"
]
```

### Experimental -> overlay_appearance [type: object] [default: {}]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"overlay_appearance": {
  "Font_Size": "16.0"
}
```

### Experimental -> subscribed_groups_clans [type: object] [default: {}]

> NO_DESCRIPTION

#### EXAMPLES:

```json
"subscribed_groups_clans": {
  "000000000000000000": {
    "name": "group_name",
    "clan_tag": "clan_tag"
  }
}
```
