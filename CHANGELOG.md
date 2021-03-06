## 2.0.6 (12-08-2021)

- After seekbar moved, video doesn't stop anymore.

## 2.0.5 (19-07-2021)

- Fix bug that when set the subtitle props and then unset andthen re-set that props, subtitle is not showing.

## 2.0.4 (19-07-2021)

- Fix bug that when the subtitle props changed, that doesn't apply to this component.

## 2.0.3 (19-07-2021)

- Remove console logs
- Edit README

## 2.0.2 (19-07-2021)

- Modify the sensitivity of seekbar

## 2.0.1 (16-07-2021)

- Fix bug that seekbar can go over the max of seekbar width
- Fix some bugs because of platform specified
- Let it restart when the video ended and then press the play button

## 2.0.0 (16-07-2021)

- Deprecate Volume
- Modify the control rendering behaviour
- Modify how it calculate and manage the seekbar position
- Improve the performance related with subtitle rendering
- Due to the changes above, following bugs were fixed automatically.
  1. When the screen orientation changed, the seekbar's position went wrong.
  2. Though controls is hided, they can be still operated because they aren't unmount. Before this change, they are just {opacity: 0} and we can still touch them.

## 1.2.3 (15-07-2021)

- Let the player be paused when seekbar moved.

## 1.2.2 (09-07-2021)

- Fix bug that the app crash when moved seekbar back far.

## 1.2.0 (09-07-2021)

- Fix bug that the app crash when moved seekbar forward far.
- Make the seek circle's touch range large.

## 1.1.0 (30-06-2021)

- MODIFIED A BUG RELATED WITH THE SEEK BAR AND SUBTITLE
  When seek bar moved to left, the subtitles didn't appear. It fixed on `v1.1.0`.

# Changed by me above (bvv8808 / hyeonwoo)

## 1.5.1 (01-11-2017)

- [Fixed deprecation of Image tag containing children](https://github.com/itsnubix/react-native-video-controls/issues/55)

## 1.5.0 (27-10-2017)

- [Added ability to remove controls](https://github.com/itsnubix/react-native-video-controls/pull/50)
- [Added ability to pass props](https://github.com/itsnubix/react-native-video-controls/pull/52)

## 1.4.1 (30-08-2017)

Bug fixes. Updated `react-native-video` to ^2.0.0 in the peer deps and `react-native` to 47.2. Changed default title font size to 14.

[#42](https://github.com/itsnubix/react-native-video-controls/issues/42)

- Related to a number of things...hitbox size, zIndex, overflow for whatever reason. Seekbar layout has been rebuilt and tested in both iOS and Android.

[#46](https://github.com/itsnubix/react-native-video-controls/issues/46)

- Props were being assigned twice. Removing second assignment has resolved the issue.

## 1.4.0 (09-08-2017)

Distilled down some merge requests and found a simple solution to a seekbar issue reported. Sometimes you just gotta give your elements a little more space. Let this be a lesson not to rush out push requests between meetings...I think this warrants a larger version change...you can now pass any prop to the `<VideoPlayer>` element and it'll pass those to `react-native-video`. API changes quite a lot because of that but shouldn't break.

## 1.3.1 (09-08-2017)

[#35](https://github.com/itsnubix/react-native-video-controls/pull/35)

- Fix flex issue with Android

[#38](https://github.com/itsnubix/react-native-video-controls/pull/38)

- Added additional RN Video params to opts call

## 1.3.0 (17-07-2017)

[#30](https://github.com/itsnubix/react-native-video-controls/issues/30)

- Add `react-native-video` as a peer-dependency

## 1.2.1 (29-06-2017)

[#26](https://github.com/itsnubix/react-native-video-controls/issues/26)

- Floor time values to prevent wrong time being displayed.

## 1.2.0 (20-03-2017)

[#14](https://github.com/itsnubix/react-native-video-controls/issues/14)

- Remove ability for loading events to be altered

[#19](https://github.com/itsnubix/react-native-video-controls/issues/19)

- Updated requirements to RN 0.42.x and RN Video 1.0.0

## 1.1.1 (23-12-2016)

Restore playInBackground and playWhenInactive

## 1.1.0 (23-12-2016)

Updated to work with react-native ^0.39.2.

### Bug fixes

[fix loadAnimation infinity loop](https://github.com/itsnubix/react-native-video-controls/pull/13)

- added if statement to loadAnimation function to prevent loop

[Crashes with New version of react-native-video](https://github.com/itsnubix/react-native-video-controls/issues/12)

- using latest github version of `react-native-video` to fix multiple issues with RN 39

## 1.0.1 (29-11-2016)

### Features

Add ability to set seeker bar colour

### Bug fixes

[When seeking sometimes seek handle hops back to original position](https://github.com/itsnubix/react-native-video-controls/issues/9)

## 1.0.0 (29-11-2016)

Bump to 1.0.0 as all major issues are fixed and API has changed slightly.

## 0.9.8 (28-11-2016)

### Bug fixes

[Seeking before onLoad triggers onEnd](https://github.com/itsnubix/react-native-video-controls/issues/8)

- modified pan handler to also look for if loading state which is set to false on init and changed when onLoad fired.

[setState being called when window off screen](https://github.com/itsnubix/react-native-video-controls/issues/7)

- added componentWillUnmount function to clear controlTimeout
- Note that if using react router componentWillUnmount will not fire unless you configure it to. See [this ticket](https://github.com/aksonov/react-native-router-flux/issues/131)

[If title is too long it runs off the page.](https://github.com/itsnubix/react-native-video-controls/issues/6)

- added flex 0.6 to size and restricted number of lines to 1. If it exceeds you'll get tail ellipsis

## 0.9.7 (21-11-2016)

### Changes

- Aesthetic changes made with regards to spacing in the bottom control group
- Tightened up space in the upper group as well.

### Features

- Changed control timeout to 15s by default. Allow the ability to overwrite. See API.
- Added ability to add container and video styling

## 0.9.6 (15-11-2016)

### Bug fixes

[Clean up file Structure](https://github.com/itsnubix/react-native-video-controls/issues/5):

- cleaned up deps and files included.

## 0.9.5 (14-11-2016)

### Bug fixes

[Tapping controls doesn't reset control hide timeout](https://github.com/itsnubix/react-native-video-controls/issues/1):

- add resets to panhandlers for volume/seek areas
- add resets to renderControl function onPress params.

[Control backgrounds should be gradients](https://github.com/itsnubix/react-native-video-controls/issues/2)

- Changed vignette assets to be more subtle.
- Added stretch to resizeMode

[Volume track bar is visible through volume icon](https://github.com/itsnubix/react-native-video-controls/issues/3)

- Rebuilt volume area to be four parts. Container (ctrls max width), track (right side of icon), fill (left side of icon) and the handle (icon).
- Added calculation to measure fill bar width and then subtract that from the width and assign to track bar on right side of icon.
- Long story short, the icon now masks the volume bar.

[Clean up file structure](https://github.com/itsnubix/react-native-video-controls/issues/5)

### Features

- Added loading icon when buffering movie
- Add error handling, ref: [Issue #4](https://github.com/itsnubix/react-native-video-controls/issues/4)
