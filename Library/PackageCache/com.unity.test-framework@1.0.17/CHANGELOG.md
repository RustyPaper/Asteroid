<svg xmlns="http://www.w3.org/2000/svg" width="96" height="96" viewBox="0 0 96 96">
  <defs>
    <style>
      .cls-1 {
        fill: #b3b3b3;
      }
    </style>
  </defs>
  <title>S_IlluPrintA3_96</title>
  <g id="ICONS_96" data-name="ICONS 96">
    <path class="cls-1" d="M75,90H21a3,3,0,0,1-3-3V9a3,3,0,0,1,3-3H57a1,1,0,0,1,0,2H21a1,1,0,0,0-1,1V87a1,1,0,0,0,1,1H75a1,1,0,0,0,1-1V27a1,1,0,0,1,2,0V87A3,3,0,0,1,75,90Z"/>
    <path class="cls-1" d="M77,24H63a3,3,0,0,1-3-3V7a1,1,0,0,1,1.707-.707l16,16A1,1,0,0,1,77,24ZM62,9.414V21a1,1,0,0,0,1,1H74.586Z"/>
  </g>
</svg>
                                                                                                                                                                                                                                                                                                                                                                                                                                                                    Introduced the capability to do a split build and run, when running playmode tests on standalone devices.
- Fixed an error in ConditionalIgnore, if the condition were not set.

## [1.0.14] - 2019-05-27
- Fixed issue preventing scene creation in IPrebuildSetup.Setup callback when running standalone playmode tests.
- Fixed an issue where test assemblies would sometimes not be ordered alphabetically.
- Added module references to the package for the required modules: imgui and jsonserialize.
- Added a ConditionalIgnore attribute to help ignoring tests only under specific conditions.
- Fixed a typo in the player test window (case 1148671).

## [1.0.13] - 2019-05-07
- Fixed a regression where results from the player would no longer update correctly in the UI (case 1151147).

## [1.0.12] - 2019-04-16
- Added specific unity release to the package information.

## [1.0.11] - 2019-04-10
- Fixed a regression from 1.0.10 where test-started events were triggered multiple times after a domain reload.

## [1.0.10] - 2019-04-08
- Fixed an issue where test-started events would not be fired correctly after a test performing a domain reload (case 1141530).
- The UI should correctly run tests inside a nested class, when that class is selected.
- All actions should now correctly display a prefix when reporting test result. E.g. "TearDown :".
- Errors logged with Debug.LogError in TearDowns now append the error, rather than overwriting the existing result (case 1114306).
- Incorrect implementations of IWrapTestMethod and IWrapSetUpTearDown now gives a meaningful error.
- Fixed a regression where the Test Framework would run TearDown in a base class before the inheriting class (case 1142553).
- Fixed a regression introduced in 1.0.9 where tests with the Explicit attribute could no longer be executed.

## [1.0.9] - 2019-03-27
- Fixed an issue where a corrupt instance of the test runner window would block for a new being opened.
- Added the required modules to the list of package requirements.
- Fixed an issue where errors would happen if the test filter ui was clicked before the ui is done loading.
- Fix selecting items with duplicate names in test hierarchy of Test Runner window (case 987587).
- Fixed RecompileScripts instruction which we use in tests (case 1128994).
- Fixed an issue where using multiple filters on tests would sometimes give an incorrect result.

## [1.0.7] - 2019-03-12
### This is the first release of *Unity Package com.unity.test-framework*.

- Migrated the test-framework from the current extension in unity.
