### 0.19.0

This release removes almost all deprecated methods.  Further, Calabash
will no longer respond to legacy environment variables.  See the
changelog/0.19.0.md for specific details.

* Launcher: restore public API for device/simulator_target? #1078
  @JoeSSS, @TeresaP
* Improve console experience #1073
* Remove 'sim location' CLI tool #1071
* Added tree feature for console #1070 @ark-konopacki
* Added briar's marks extension for irbc #1068 @ark-konopacki
* Complete switch to run loop 2.1.0 interface #1069
* Change Map module to class and provide class methods #1065 @svandeven
* Use tap_keyboard_action_key instead of done #1057 @lucatorella
* Launcher#check_server_gem_compatibility should be a post-launch check
  #1051
* Launcher: use RunLoop 2.1.0 APIs where possible #1050
* Core: remove references to @calabash_launcher Cucumber World variable
  #1049
* Deprecate Launcher#calabash_notify #1048
* Deprecate old Launcher behaviors and use new RunLoop APIs in #relaunch
  #1047
* Launcher: deprecated #default_uia_strategy #1046
* Move http methods out of launcher #1044
* Rotation: remove playback API - since 0.16.2 #1040
* Replace NO_STOP with QUIT_APP_AFTER_SCENARIO #1038
* Unify logging between RunLoop and Calabash #1035
* Gem: remove deprecated.rb #1034
* Remove more deprecated Device behaviors #1033
* Remove CALABASH_VERSION_PATH #1028
* Remove unnecessary methods from Launcher #1027
* Remove deprecated methods for 0.19.0 #1026
* Remove the Playback API #1025
* Remove deprecated XcodeTools, PlistBuddy, and SimulatorAccessibility
  #1024
* Remove deprecated methods from KeyboardHelpers #1023
* Remove deprecated ENV variables and constants #1022
* Core: undeprecate #set_text #1021
* CLI: remove 'update' command #1020
* Remove sim_launcher gem dependency and SimulatorLauncher class #1016
* Remove KeyboardHelpers.done #1004
* Screen coordinates are incorrect when running in Zoomed mode #998
* Remove the sim_launcher dependency #921
* Cannot query UIWebView by accessibilityIdentifier or
  accessibilityLabel #735

### 0.18.2

* Replace automatic .app detection with RunLoop implementation #1011
* Gem: pin rake to ~> 10.5; rspec 3.4 is not compatible #1010
* Launcher: remove TCC privacy settings #1009
* Keyboard: log that #done is going to be removed #1007
* Launcher: fix error reporting in #new\_run\_loop #1006

### 0.18.1

* CLI: use RunLoop::Ipa or RunLoop::App for version check #996
* Update skeleton support/dry\_run to load predefined steps #995
* Fix formatter import problem #994
* SimLauncher: fix autodetection of app bundle #974 @ark-konopacki

### 0.18.0

This release contains a new version of the server that provides
iframe support for css selectors.

* Fix `sim locale` command line tool #987
* Added Calabash.podspec #979 @ark-konopacki

### 0.17.1

This release contains a new version of the server that fixes
scrolling in WebViews.

* Launcher#reset\_simulator should call RunLoop::CoreSimulator.erase #975
  @ark-konopacki
* Remove the lib/calabash directory and put Dylibs module in
  Calabash::Cucumber #967
* Use run loop cache for all strategies when attaching #960
* Track GitLab CI #958
* Don't immediately return true for simulator? if simulator\_details is
  empty #957 @MikeNicholls
* Tracker: catch errors and log them to a file #954
* Tracker: add missing requires to avoid throwing errors #952
* Use UIAutomation JavaScript to touch keyboard Delete key #942 @MikeNicholls

### 0.17.0

This release contains several changes that are not backward compatible.

* requires ruby >= 2.0
* the backdoor API has become more flexible, but some users will find
  existing backdoors no longer work or behave in unexpected ways
* RESET_APP_BETWEEN_SCENARIOS no longer resets the simulator, it only
  resets the app sandbox.  The reset_app_sandbox method has been
  deprecated; it is now a no op. See #878 for details.

This release adds user tracking.

* Launcher: post usage data at relaunch #937
* Store user preferences in ~/.calabash/preferences/preferences.json
  #933
* Fix the "reset app sandbox between Scenarios" behavior #923
* RESET_APP_BETWEEN_SCENARIOS is still resetting the simulator not just
  the app sandbox #878
* Gem: min run-loop version is 2.0 #919
* Calabash can manage a ~/.calabash directory #909
* Docs: minor versions can contain breaking changes #905
* Gem: allow any version of cucumber #904
* Add client for shake route #902 @tommeier
* send_app_to_background uses "suspend" server route #901
* Update backdoor method to handle new LPBackdoorRoute behavior #894
* README rewrite for 0.17 #892
* Drop ruby 1.9 support; >= 2.0 is required #883
* Update the features skeleton #882
* Fixing wiki link for updating calabash version #869 @yakovsh

### 0.16.4

This is a patch release for the server.  Xcode 7.0.1 introduced
new rules for embedding bitcode in libraries.  The Objective-C
libraries included in this release are compatible with these
new rules.

* Improve server build rake task to complement the new server build system #864

