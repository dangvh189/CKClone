# CHANGELOG
All notable changes to this project will be documented in this file.

## [Unreleased]

## [0.0.1] - 2021-04-02
### Added
- Initial Version

## [0.0.2] - 2021-05-05
### Added
- AppleLogger

### Modified
- Existing scripts moved under `Editor` directory

## [0.0.3] - 2021-05-07
### Modified
- AppleLogger now forwards logs from all threads to NSLog

## [0.0.5] - 2021-07-29
### Modified
- AppleBuildProfile DefaultProfile creation properly creates sub-asset AppleBuildSteps
- Loading DefaultProfile from disk loads all assets

## [0.0.6] - 2021-08-13
### Modified
- UserManagement is disabled by default
- BuildSteps appear in alphabetical order

## [0.0.7] - 2021-10-26
### Modified
- DefaultAppleBuildProfile deserialization / discovery issue resolved

## [0.0.8] - 2022-03-28
### Modified
- Support for multiple minimum OS version definitions in Build Settings
- Update native project with bundle ID fixes
- Updating native project with aggregate build targets and supporting schemes
- Added library processor to ensure correct framework settings on import
- Added utility function to find correct library paths based upon name and BuildPlatform

## [0.0.9] - 2022-04-07
### Modified
- AppleBuildProfile editor uses SerializedObject / SerializedProperty paradigm

## [0.0.10] - 2022-04-07
### Modified
Big update to the native library processor

- Now only processes frameworks with bundle IDs that start with 'com.apple-plugins.'
- Native library logging is coalesced into a single Unity Debug.Log() call to avoid tons of Console spew
    - Plus, output is formatted nicely!
- Full debug log is only output in development builds
    - As configured in Unity project settings
    - Can be overriden with bool in source. (See: AppleNativeLibraryProcessor.cs) 
- Library processor skips processing on libraries found in packages
    - Can be forced with bool in source. (See: AppleNativeLibraryProcessor.cs)
