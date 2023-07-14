# SomeGeetha music player


<!-- Logo -->

SomeGeetha is an open source music player for Android, allowing you to play music from multiple
services : files on your phone, [Spotify], and more.

SomeGeetha is available on [Google Play], or [here on GitHub].
It seems to also be on [IzzySoft F-Droid], and to stay up to date there.

Other repos like ~~[Aptoide]~~ or even ~~[ApkPure]~~, ~~[ApkCombo]~~ are not recommended because
they don't seem
to stay up to date fast, and i can't check if they modified the `apk` before publishing it.

<div align="center" style="text-align: center;">
  <img src="https://valou3433.fr/blade0.png" width="350" style="max-width: 350;"/>
  <img src="https://valou3433.fr/blade1.png" width="350" style="max-width: 350;"/>
</div>

## Feature overview

SomeGeetha music Player is developed by me ([@vhaudiquet]) alone, so the project cannot be tested on many
devices and scenarios ; if you find an issue, open one here.

- The app will open on your library, categorized as Artists, Albums, Songs, and Playlists (available
  in the navigation drawer).
- It allows you to manage libraries for songs (add/remove from source library) and playlists (
  add/remove from playlist, create/remove playlists)
- It supports Android 'dark theme' (the screenshots above are done on a dark themed system).
- It is completely free (there are no ads, no limited version)
- It caches the library locally, so launching SomeGeetha requires virtually no data (only refreshing
  tokens and status of sources servers)
- **(TODO)** It has a 'data saving' mode that allows you to listen to music while consuming very low
  mobile data (by not loading album arts)
- The search feature allows you to search the local library instantly
- The "explore" mode allows you to search and browse sources for new music (for example
  search all Spotify and look for new releases)
- It has a layout that can adapt for tablet users (landscape layout)
- It is available in different languages : English, French, German, Turkish ([and you can easily help me traduce it](CONTRIBUTING.md))

<div align="center" style="text-align: center;">
  <img src="https://valou3433.fr/bladef0.png" width="200" style="max-width: 200;"/>
  <img src="https://valou3433.fr/bladef1.png" width="200" style="max-width: 200;"/>
  <img src="https://valou3433.fr/bladef2.png" width="200" style="max-width: 200;"/>
</div>

<div align="center" style="text-align: center;">
  <img src="https://valou3433.fr/bladelandscape.png" width="600" style="max-width: 600;"/>
</div>

### Supported services (music sources)

- Local (i.e. files on your phone)
- Spotify

### About Spotify

You will need a **Spotify Premium** account to play music from [Spotify], but you can use SomeGeetha
without a premium account (to play your Spotify playlists from other sources, for example)

Blade is using the official [Spotify Android Auth] library and [Retrofit] to access
the [Spotify Web API], i.e. to obtain user library and playlists. In order to play music from
Spotify, SomeGeetha uses the [librespot-java] library.

For now, SomeGeetha will act as a Spotify Connect peripheral. **Please do not try to control SomeGeetha with
Spotify Connect**. It won't work, and it will glitch the app.

When connecting SomeGeetha and Spotify, i am for now obligated to ask directly for your username and
password, 2 times : one for [librespot-java], which requires them directly (Spotify does not allow
streaming music from their API authentification), and one for [Spotify Android Auth], which uses the
secure OAuth2 protocol. I can only promise you that i am not stealing your credentials ; if you are
paranoid, you may build SomeGeetha from sources or use a network analyzer to see that all network traffic
goes to [Spotify] servers.

Special thanks to the people at [librespot-org] and [librespot-java] ; without them, Spotify support
would not have been possible.

## Future updates

New features and bug fixes or improvements are coming. Here is a list of what i want to implement :

- SPOTIFY: Use Android Native Decoders, and/or libtremolo if native decoder not present
- UI: Show albums in an 'album view' instead of a list
- Add new services : SoundCloud, YouTube Music, Amazon Music, Tidal, WebDAV/FTP Servers...
- CORE: 'SomeGeetha' playlists, that can contain song from all sources

## Contributing

See [CONTRIBUTING.md]

## Older versions

