---
title: Adding the game
order: 3
menu: child
---

To manage games and their versions, you should switch to **Development Mode**. In the upper left corner of the page in your personal account, from the ARVI VR drop-down menu, select **Development**.

<img src="{{ '/assets/img/development-mode.png' | relative_url }}" class="img-fluid mx-auto d-block" />

<a name="creating-game-description"></a>
# Creating game description
Go to the [**Games**](https://vrp.arvilab.com/development/games) section -- this is a list of your games. From here you can manage everything related to the game -- add / change a description, manage game versions, distribute it across locations, etc. To create a new game, click **New** at the top right of the page.

<a href="{{ '/assets/img/game-new.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-new.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

You must fill the game fields:

| {::nomarkdown}<div style="width:180px">{:/}Field{::nomarkdown}</div>{:/} | Description |
| --- | --- |
| **`Name`** | Name of the game. Used for internal platform purposes and not visible to users. May match the **`Display name`** field. Maximum `255` characters. |
| **`Display name`** | The displayed name of the game. Used for display on site pages, in the list of marketing materials, etc. Maximum `255` characters. |
| *`Release`* | Expected release date or development status. For example: `01.01.2022` or` Winter 2022` or `Coming Soon`. Displayed on the site in the game information. Optional field. |
| **`Site`** | The URL of the game description page. Maximum `2048` characters. |
| **`Poster`** | Game poster file. The poster is displayed on the site in the game description. |
| **`Short description`** | A short description of the game in English. Maximum `1000` characters. |
| **`Long description`** | A detailed description of the game in English. Maximum `4000` characters. |
| **`Type`** <a name="game-type-field">| Content type: game or tutorial. |
| **`Status`** <a name="game-status-field">| Game activity status. If the game is in the `Active` status, it is available to everyone, according to the distribution by location. If `Inactive` -- the game is not distributed and is displayed only for developer. |
| **`Priority`** | Will be used in a future version of the platform. Default value: `100`. |
| **`Download Attempts`** | Will be used in a future version of the platform. Default value: `3`. |
| **`Can Use Low Space`** | Will be used in a future version of the platform. Default value: `OFF`. |
| **`Key`** <a name="game-key"></a> | Game key. It is generated automatically for each game and is used by the developer when integrating the ARVI SDK. |

For example, this is how these settings look for one of our games -- Archer.

<img src="{{ '/assets/img/game-info.png' | relative_url }}" class="img-fluid mx-auto d-block" />

<a name="game-promo-materials"></a>
# Adding promotional materials
Promotional materials allow location owners to use your game posters, logos, descriptions, etc. on their websites. These materials will be used to advertise the game and display information on gaming locations.  
To upload promotional materials, go to the [**Games**](https://vrp.arvilab.com/development/games) section and select **Materials** from the game menu.

<a href="{{ '/assets/img/game-materials.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-materials.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

## Description
On the **Description** tab fill in the localized detailed game descriptions for each language. Among other things, it will also used for social media, press release, etc.

<img src="{{ '/assets/img/materials-description.png' | relative_url }}" class="img-fluid mx-auto d-block" />

## Promo materials
On the **Promo materials** tab add graphic materials: game promo art (vertical), screenshots (horizontal), logo (with transparency), poster, etc. It is recommended to name the files sequentially. For example screenshot1.png, screenshot2.png, etc. Below are the recommended sizes for promo materials:

| Promo materials | Sizes |
| :------------- | :------------- |
| `WEB BANNERS` | 300x250 px / 300x600 px / 320x10 px / 336x280 px / 728x900 px |
| `PROMO ART` | 2048x2048 px |
| `SCREENSHOTS` | 1920x1080 px / 5120x2160 px / 2048x864 px / 2560x1080 px |
| `LOGOTYPES` | 1868x1046 px |
| `POSTER` | A1 (84.1х59.4 сm / 33.1x23.4 ") |
| `WALLSIZE BANNERS` | 6x2.5 m / 19.69x8.2 ft |

<img src="{{ '/assets/img/materials-promo-art.png' | relative_url }}" class="img-fluid mx-auto d-block" />
<img src="{{ '/assets/img/materials-screenshots.png' | relative_url }}" class="img-fluid mx-auto d-block" />

## Source materials
On the **Source materials** tab add the zip archives with the source files of the graphic materials (`PSD` files with layers), if any. This will help the location owners add their logos to the graphic materials or adjust your materials for their needs.

<img src="{{ '/assets/img/materials-source-materials.png' | relative_url }}" class="img-fluid mx-auto d-block" />

## Video materials
On the **Video materials** tab you can add game trailers (about a minute in length) and short gameplay videos. You need to provide a link to the video on youtube and download the original video file in `MP4` format.

<img src="{{ '/assets/img/materials-video.png' | relative_url }}" class="img-fluid mx-auto d-block" />

## Photo booth materials
This section is temporarily not used.

<a name="creating-manifest"></a>
# Creating game manifest
The manifest allows the platform to find out what capabilities a specific version of the game supports: with what parameters to launch it, how many players it is designed for, what localizations it supports, and much more. Each time you create a new version of your game on the platform, you will specify a manifest for it. The manifest characterizes the capabilities of a specific version of the game, not the game as a whole.
For example, in the new version of the game you added support for the new localization, but previous versions do not support it. Or you decided to add new in-game commands to the game, which did not exist before. In this case, you will create a new, updated manifest for this version. Thus, a game can have multiple manifests, each describing a specific version or multiple versions.
Manifests for games are stored in the [**Manifests**](https://vrp.arvilab.com/development/manifests) section -- there you can view and change existing manifests and create new ones by clicking the **New** button.

<a href="{{ '/assets/img/manifest-new.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/manifest-new.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

You must fill the manifest fields:

| {::nomarkdown}<div style="width:180px">{:/}Field{::nomarkdown}</div>{:/} | Description |
| --- | --- |
| **`Name`** | The name of the manifest. You can name it by the name of the game and version. For example: `$PROJECT_NAME Manifest v1`, where `$PROJECT_NAME` is the name of the game. Maximum `255` characters. |
| *`Tutorial`* | If the game has a separate tutorial registered earlier, then in this drop-down list you can specify the tutorial for the game. |
| **`Exe Path`** | The relative path to the game executable file. Indicated relative to the root folder of the game. For example, for Unity games, this is the executable file `$PROJECT_NAME.exe` located in the root of the game folder. For Unreal games, this is `$PROJECT_NAME\Binaries\Win64\$PROJECT_NAME-Win64-Shipping.exe`. |
| **`Icon`** | Manifest icon file. |
| *`Server Options`* <a name="manifest-server-options"></a> | Command line parameters that must be passed to a multiplayer game to start as Server (if supported by the game). The developer himself, at his discretion, forms this string as it is convenient for him, using the [variables](#variables-description) described below. |
| *`Client Options`* | Command line parameters that must be passed to a multiplayer game to start as Client (if supported by the game). The developer himself, at his discretion, forms this string as it is convenient for him, using the [variables](#variables-description) described below. |
| *`Single Player Options`* | Command line parameters that must be passed to the game to run in singleplayer mode. The developer himself, at his discretion, forms this string as it is convenient for him, using the [variables](#variables-description) described below. |
| *`Single-player Only`* | If the game does not support multiplayer and is designed for single player only, you must set the value to `ON`. Default value: `OFF`. |
| **`Game Timeout`** <a name="manifest-game-timeout"></a> | Game session time limit in seconds. If this limit is reached, the game should be closed. In this field, the developer specifies a default value (usually `3600`), however, it can be changed dynamically by the operator before starting the game. |
| **`Min Players`** | The minimum number of players supported by the game. |
| **`Max Players`** | The maximum number of players supported by the game. |
| *`Is Tutorial`* | If this manifest is for a game of type `Tutorial` ([**`Type`**](#game-type-field) field in game description), then this field must be set to` ON`. In all other cases, use the default value: `OFF`. |
| *`Teams`* | If the game supports splitting into teams, then this field must be set to `ON`. In all other cases, use the default value: `OFF`. |
| *`Free Roam`* | If the game supports Free Roam, then this field must be set to `ON`. If not, use the default value: `OFF`. |
| *`Lobby`* | Temporarily unused, leave blank. |
| *`Fast Start`* | If the game supports launching Clients before starting the Server, this can shorten the session start time. |
| *`Spectator Supported`* | If the game supports spectator mode, then this field must be set to `ON`. |
| *`SteamVR Grid`* | Allows to override the SteamVR grid settings (appearance and color) for the game. |
| *`SteamVR Graphics`* | Allows to override the SteamVR graphics settings for the game. |
| *`Voice Chat Level`* | Allows to override the audio chat volume. |
| *`Height & Width`* | Allows to set the size of the play area if the *`Free Roam`* field is set. |
| *`Fixed Tracker Number`* | Allows to set the number of trackers if the *`Free Roam`* field is set. |

<a name="variables-description"></a>
In the *`Server Options`*, *`Client Options`* and *`Single Player Options`* fields, it is allowed to use variables that the platform will replace with specific values before starting the game:

| {::nomarkdown}<div style="width:200px">{:/}Variable{::nomarkdown}</div>{:/} | Description |
| --- | --- |
| `[$PLAYERS_COUNT]` | Number of players participating in the game session. |
| `[$LANGUAGE]` | The language selected before starting the game in the "en" format. |
| `[$SESSION_TIME]` | The specified game session time in **minutes**. If not changed by the operator, then by default the [**`Game Timeout`**](#manifest-game-timeout) field value will be substituted, converted into minutes. |
| `[$SESSION_GUID]` | Game session ID. |
| `[$CORD_TWISTING_DISABLE]` | Use if the game **has** protection against cable twisting (uses ShouldApplicationTrackCordTwisting property or ShouldApplicationTrackCordTwisting () function in the SDK). |
| `[$SERVER_IP]` | Game server IP address. |

For example, the *`Server Options`* field is written as follows:  
* -players=[$PLAYERS_COUNT] -language=[$LANGUAGE] -session_time=[$SESSION_TIME]*  
In this case, if the operator creates a game session for two in English with a time limit of 30 minutes, the game will start with the command line parameters  
* -players=2 -language=EN -session_time=1800*  

*`Server Options`* examples:  
* -type=server -players=[$PLAYERS_COUNT] -language=[$LANGUAGE] -session_time=[$SESSION_TIME] -session_id=[$SESSION_GUID] [$CORD_TWISTING_DISABLE]
* -culture=[$LANGUAGE] --server_ip=listen --session_time=[$SESSION_TIME] [$CORD_TWISTING_DISABLE]

*`Client Options`* examples:  
* -type=client -server_ip=[$SERVER_IP] -language=[$LANGUAGE] -session_time=[$SESSION_TIME] -session_id=[$SESSION_GUID] [$CORD_TWISTING_DISABLE]
* -culture=[$LANGUAGE] --server_ip=[$SERVER_IP] --session_time=[$SESSION_TIME] [$CORD_TWISTING_DISABLE]

*`Single Player Options`* examples:
* -language=[$LANGUAGE] --session_time=[$SESSION_TIME] [$CORD_TWISTING_DISABLE]
*  -type=server -players=1 -language=[$LANGUAGE]
* -culture=[$LANGUAGE] --session_time=[$SESSION_TIME]

You can also create a manifest based on an existing one. For example, you added support for a new language, a new in-game command, or changed the launch parameters of the game. In order not to fill in all the fields again, you can duplicate the existing manifest and change the necessary settings. To do this, in the manifest menu, select **Duplicate** -- a copy of the manifest will be created, it remains to give it a new name.

<img src="{{ '/assets/img/manifest-duplicate.png' | relative_url }}" class="img-fluid mx-auto d-block" />

<a name="manifest-localizations"></a>
## Setting up localizations
In the manifest, you can indicate which languages the game supports. This list will be displayed in the admin panel, allowing the operator to select the game session language before launching. The selected language can then be passed to the game as a command line parameter in the [*`Server / Client / Single Player Options`*](#manifest-server-options) fields.
To configure localizations, select the appropriate manifest from the [**Manifests**](https://vrp.arvilab.com/development/manifests) section and select **Languages** from its menu. On the page with a list of languages, check the ones that the game supports.

<img src="{{ '/assets/img/manifest-languages.png' | relative_url }}" class="img-fluid mx-auto d-block" />

<a name="manifest-ingame-commands"></a>
## In-game commands
In-game commands are commands that the game provides to control the gameplay from the outside. These commands are displayed in the operator's admin panel and enable him to control the game remotely. For example, using such commands, the operator can add game time, skip a puzzle, load a certain level, etc. The game developer himself decides what commands he is ready to provide for management, and he himself implements this in the game.  
To create or edit the list of in-game commands, go to the [**Manifests**](https://vrp.arvilab.com/development/manifests) section, select a manifest and select **In-Game Commands** from its menu.

<img src="{{ '/assets/img/manifest-commands.png' | relative_url }}" class="img-fluid mx-auto d-block" />

In-game commands have a nested structure and looks like a menu. **Root commands** are at the root of the list and do not contain nested commands. **Folders** are also located at the root of the list and contain **nested commands**. The folders themselves are not commands and are only used to group the commands nested within them.

<a href="{{ '/assets/img/game-commands.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-commands.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

To add a **root command** or **folder** press **New root command** or **New folder** respectively.

<a href="{{ '/assets/img/game-commands-new.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-commands-new.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

Complete the following fields :

| {::nomarkdown}<div style="width:180px">{:/}Field{::nomarkdown}</div>{:/} | Description |
| --- | --- |
| **`Name`** | The name of the command / folder that will be displayed for the operator in the admin panel. |
| *`Description`* | Command / folder description. |
| **`Command Url`** | Command URL, used to send from the admin panel to the game. You yourself come up with this UR, it will be used when processing a command in the game. Read more about this in the SDK Integration Guide. <br> Parameters can be passed in the common form of URL: /commandName?Param1=value1&param2=value2. <br> Not used when creating folders. |
| **`Icon`** | Icon for displaying the command / folder in the admin panel. Recommended size is `256x256`. |
| **`Target`** | Indicate who you want to send the command to -- the selected player, the game server, or everyone in the game. <br> Not used when creating folders.|
| *`Order`* | The number under which the command / folder will be located in the general list of commands. Both positive and negative numbers are allowed. The lower the number, the higher the command / folder will be in the list. |
| *`Activation Message`* | A message that when sent from the game using the `ActivateInGameCommand` method (see SDK Integration Guide) activates the command / folder (or several commands, if the value of this field is the same for them), i.e. will display it in the list. The developer himself comes up with the name of this message. |
| *`Deactivation Message`* | A message that, when sent from the game using the `DeactivateInGameCommand` method (see SDK Integration Guide), deactivates the command / folder (or several commands, if the value of this field is the same for them), i.e. will hide it in the list. The developer himself comes up with the name of this message. |

Folder actication affects the state of the commands nested in it. If the folder is deactivated, all nested commands will also be deactivated. If you activate it after that, the nested commands will return to the state in which they were before.  
Commands and folders for which the *`Activation Message`* field is **not specified** will initially be **active** (i.e. displayed) in the admin panel. And vice versa -- the commands for which you **fill in** this field will be initially **disabled**, and to activate them you will need to execute the `ActivateInGameCommand` method in the game. The same goes for folders.

<a name="creating-new-version"></a>
# Creating a new game version and uploading files
After creating the game description and manifest, you need to create the first game version. You will also need to create new versions in case you want to update the game. To do this, use the [Build Uploader]({{ '/tabs/downloads-dev-tools/' | relative_url }}) utility. After its launch and authorization, select the **Upload** mode.

<a href="{{ '/assets/img/build-uploader-upload.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/build-uploader-upload.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:500px;width:100%;" /></a>

Fill all the required version fields and click **Upload**. Your game will be automatically packed into an archive, split into parts and uploaded to our website.

<a href="{{ '/assets/img/build-uploader.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/build-uploader.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:500px;width:100%;" /></a>

<a name="game-activation"></a>
# Game activation
When your game is ready for release, you need to activate it. To do this, go to the [**Games**](https://vrp.arvilab.com/development/games) section and select **Edit** in the game menu and change the [**`Status`**](#game-status-field) field to `Active`.

<a href="{{ '/assets/img/game-edit.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-edit.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

<img src="{{ '/assets/img/game-activate.png' | relative_url }}" class="img-fluid mx-auto d-block" />

<a name="game-distribution"></a>
# Distribution by locations
Now you can distribute your game versions between locations. For example, you can distribute a stable version to one of the locations, and a test version to another location. To do this, go to the [**Games**](https://vrp.arvilab.com/development/games) section and select **Distribute** from the game menu.

<a href="{{ '/assets/img/game-distribute.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-distribute.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

<a href="{{ '/assets/img/game-distribution.png' | relative_url }}" data-toggle="lightbox"><img src="{{ '/assets/img/game-distribution.png' | relative_url }}" class="img-fluid mx-auto d-block" style="max-width:700px;width:100%;" /></a>

In the **Builds** list, select the version you want to distribute.  
If you want to add this version to a specific location, in the list of **Available Locations**, click **Add** next to the one to which you want to distribute the game. Now, when the games are updated at this location, your game will be added there or updated to the selected version.  
If you need to remove a version from a specific location, in the list of **Enabled Locations**, click **Remove** next to the location where you want to remove the game. The next time you update games in this location, it will be deleted.
