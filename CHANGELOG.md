## Changelog

[简体中文](docs/CHANGELOG.zh-Hans.md)

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## TOC

- [[Unreleased]](#Unreleased)
  - [Added](#addedunreleased)
  - [Changed](#changedunreleased)
- [[0.4.1-alpha] - 2019-07-11](#041-alpha---2019-07-11)
  - [Added](#added041-alpha)
  - [Changed](#changed041-alpha)
- [[0.4.0-alpha] - 2019-02-17](#040-alpha---2019-02-17)
  - [Changed](#changed040-alpha)

Click up arrow to go back to TOC.

### [Unreleased]

#### Added(Unreleased)

- Add arguments for min and max region size. [issue #3](https://github.com/BingLingGroup/autosub/issues/3)
- Add metadata.py. [issue #5](https://github.com/BingLingGroup/autosub/issues/5)
- Add output file name detection to avoid any file overwritting.
- Add new dev branch for latest dev codes to push.
- Add more output format(ass, ssa, sub, mpl2, tmp). [issue #20](https://github.com/BingLingGroup/autosub/issues/20)

#### Changed(Unreleased)

- [issue #5](https://github.com/BingLingGroup/autosub/issues/5).
  - Rewrite help messages.
  - Refactor argparse.
  - Refactor constaints.
- Change dev branch into origin branch.
- Use alpha branch for alpha releases.
- Change docs.
- Change audio conversion workflow to get a better audio quality to process. Currently will create two files from the original source file separately. 48kHz/16bit/mono .wav for local speech regions finding. 44.1kHz/24bit/mono .flac for google speech v2 api upload or in other words, speech recognition. Need to point out that [Google-Speech-v2](https://github.com/gillesdemey/google-speech-v2) is wrong on the supported .flac audio channel number. According to my test the api doesn't support the 2-channel .flac file. [agermanidis/autosub issue #155](https://github.com/agermanidis/autosub/issues/155)
- Refactor internal regions unit to millisecond. [issue #23](https://github.com/BingLingGroup/autosub/issues/23)
- Refactor speech regions detection by using auditok. [issue #27](https://github.com/BingLingGroup/autosub/issues/27)

<escape><a href = "#TOC">&nbsp;↑&nbsp;</a></escape>

### [0.4.1-alpha] - 2019-07-11

[0.4.1-alpha release](https://github.com/BingLingGroup/autosub/releases/tag/0.4.1-alpha)

#### Added(0.4.1-alpha)

- Add https speech-to-text api url and url choice argument. [agermanidis/autosub pull request #135](https://github.com/agermanidis/autosub/pull/135)
- Add external speech-to-text regions control from external subtitle files. [agermanidis/autosub pull request #159](https://github.com/agermanidis/autosub/pull/159)
- Add scripts to build, release and etc.

#### Changed(0.4.1-alpha)

- Fix vague language codes caused wrong recognition result. [agermanidis/autosub pull request #136](https://github.com/agermanidis/autosub/pull/136)
- Change docs.

<escape><a href = "#TOC">&nbsp;↑&nbsp;</a></escape>

### [0.4.0-alpha] - 2019-02-17

[0.4.0-alpha release](https://github.com/BingLingGroup/autosub/releases/tag/0.4.0-alpha)

#### Changed(0.4.0-alpha)

- Fix several issues. [agermanidis/autosub pull request #128](https://github.com/agermanidis/autosub/pull/128) by [@iWangJiaxiang](https://github.com/iWangJiaxiang)
  - Fix "ffmpeg.exe" causes "Dependency not found: ffmpeg" on Windows.
  - Fix "ValueError" when the response data of "SpeechRecognizer" couldn't be parsed to JSON Object.
  - Fix Temp Folder Permissions Denied on Windows 10. [agermanidis/autosub issue #15](https://github.com/agermanidis/autosub/issues/15)
- Fix JSONDecodeError caused crash. [agermanidis/autosub pull request #131](https://github.com/agermanidis/autosub/pull/131) by [@raryelcostasouza](https://github.com/raryelcostasouza)

<escape><a href = "#TOC">&nbsp;↑&nbsp;</a></escape>