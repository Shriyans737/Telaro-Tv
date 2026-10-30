# Telaro

**A fast, simple home screen for Android TV.**

Your apps in a clean grid, built for the remote. Open source. One press to go back.

![Telaro home screen](docs/screenshot.png)

## What you get

- **Your apps, front and center.** A clean 5-column grid of everything installed.
- **Made for the remote.** A clear highlight follows the D-pad.
- **Opens any app.** Press OK and it opens.
- **Home screen ready.** Use it as your TV's home screen.
- **Easy way back.** Pick *Original Home* and your normal home screen returns.
- **Private.** No ads, no accounts, no tracking.

## Install

You need an Android TV or Google TV (Android 8 or newer) and a computer on the same Wi-Fi with [adb](https://developer.android.com/tools/releases/platform-tools).

1. **On the TV**, turn on developer mode: Settings → System → About → press *Android TV OS build* 7 times. Then Settings → System → Developer options → turn on **USB debugging**. Note the TV's IP address (Settings → Network & Internet).
2. **On your computer**, download `Telaro.apk` from the [latest release](https://github.com/YOUR-USERNAME/telaro/releases/latest) and run:

   ```
   adb connect 192.168.1.50:5555
   adb install -r Telaro.apk
   ```

   Swap in your TV's IP address. If the TV asks *Allow USB debugging?*, tick *Always allow*.
3. **On the TV**, open **Telaro** from the apps list.

If Google Play Protect blocks the install, choose *More details* → *Install anyway*.

## Going back

Select **Original Home** in Telaro to switch back to your normal home screen.

To remove Telaro completely:

```
adb uninstall com.telaro.tv
```

## Build it yourself

You need JDK 17, the Android SDK (platform 34) and adb.

```
./build.sh
```

This creates `Telaro.apk` in the project folder. Keep your own `telaro.keystore` and `keystore.properties` private, since updates must be signed with the same key.

## Roadmap

- [x] Apps grid with remote focus
- [x] Open apps with OK
- [x] Home screen mode with *Original Home*
- [ ] Clock and day/night look
- [ ] Trending picks
- [ ] Weather
- [ ] Screensaver

## License

[MIT](LICENSE). Fork it, change it, ship it.

Not affiliated with Google or any TV brand. Android and Android TV are trademarks of Google LLC.
