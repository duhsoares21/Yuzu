<!--
SPDX-FileCopyrightText: 2018 yuzu Emulator Project
SPDX-License-Identifier: GPL-2.0-or-later
-->

<h1 align="center">
  <br>
  <a href="https://yuzu-emu.org/"><img src="https://raw.githubusercontent.com/yuzu-emu/yuzu-assets/master/icons/icon.png" alt="yuzu" width="200"></a>
  <br>
  <b>yuzu</b>
  <br>
</h1>

<h4 align="center"><b>yuzu</b> is the world's most popular, open-source, Nintendo Switch emulator — started by the creators of <a href="https://citra-emu.org" target="_blank">Citra</a>.
<br>
It is written in C++ with portability in mind, and we actively maintain builds for Windows, Linux and Android.
</h4>

<p align="center">
    <a href="https://dev.azure.com/yuzu-emu/yuzu/">
        <img src="https://dev.azure.com/yuzu-emu/yuzu/_apis/build/status/yuzu%20mainline?branchName=master"
            alt="Azure Mainline CI Build Status">
    </a>
    <a href="https://discord.com/invite/u77vRWY">
        <img src="https://img.shields.io/discord/398318088170242053?color=5865F2&label=yuzu&logo=discord&logoColor=white"
            alt="Discord">
    </a>
</p>

<p align="center">
  <a href="#compatibility">Compatibility</a> |
  <a href="#development">Development</a> |
  <a href="#building">Building</a> |
  <a href="#download">Download</a> |
  <a href="#support">Support</a> |
  <a href="#license">License</a>
</p>

## Compatibility

The emulator is capable of running most commercial games at full speed, provided you meet the [necessary hardware requirements](https://yuzu-emu.org/help/quickstart/#hardware-requirements).

For a full list of games yuzu supports, please visit our [Compatibility page](https://yuzu-emu.org/game/).

Check out our [website](https://yuzu-emu.org/) for the latest news on exciting features, monthly progress reports, and more!

## Development

Most of the development happens on GitHub. It's also where [our central repository](https://github.com/yuzu-emu/yuzu) is hosted. For development discussion, please join us on [Discord](https://discord.com/invite/u77vRWY).

If you want to contribute, please take a look at the [Contributor's Guide](https://github.com/yuzu-emu/yuzu/wiki/Contributing) and [Developer Information](https://github.com/yuzu-emu/yuzu/wiki/Developer-Information).
You can also contact any of the developers on Discord in order to know about the current state of the emulator.

If you want to contribute to the user interface translation project, please check out the [yuzu project on transifex](https://www.transifex.com/yuzu-emulator/yuzu). We centralize translation work there, and periodically upstream translations.

## Building

* __Windows__:

<div id="wiki-content" class="mt-4">
      <div data-view-component="true" class="Layout Layout--flowRow-until-md Layout--sidebarPosition-end Layout--sidebarPosition-flowRow-end">
  <div data-view-component="true" class="Layout-main">          <div id="wiki-body" class="gollum-markdown-content">
              <div class="markdown-body">
                <div class="markdown-heading"><h1 class="heading-element">THIS GUIDE IS INTENDED FOR DEVELOPERS ONLY, SUPPORT WILL ONLY BE GIVEN IF YOU'RE A DEVELOPER.</h1><a id="user-content-this-guide-is-intended-for-developers-only-support-will-only-be-given-if-youre-a-developer" class="anchor-element" aria-label="Permalink: THIS GUIDE IS INTENDED FOR DEVELOPERS ONLY, SUPPORT WILL ONLY BE GIVEN IF YOU'RE A DEVELOPER." href="#this-guide-is-intended-for-developers-only-support-will-only-be-given-if-youre-a-developer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading"><h2 class="heading-element">Method I: MSVC Build for Windows</h2><a id="user-content-method-i-msvc-build-for-windows" class="anchor-element" aria-label="Permalink: Method I: MSVC Build for Windows" href="#method-i-msvc-build-for-windows"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading"><h3 class="heading-element">Minimal Dependencies</h3><a id="user-content-minimal-dependencies" class="anchor-element" aria-label="Permalink: Minimal Dependencies" href="#minimal-dependencies"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p>On Windows, all library dependencies are automatically included within the <code>externals</code> folder, or can be downloaded on-demand. To build yuzu, you need to install:</p>
<ul>
<li>
<strong><a href="https://web.archive.org/web/20240304183509/https://visualstudio.microsoft.com/downloads/" rel="nofollow">Visual Studio 2022 Community</a></strong> - <strong>Make sure to select C++ support in the installer. Make sure to update to the latest version if already installed.</strong>
</li>
<li>
<strong><a href="https://web.archive.org/web/20240304183509/https://cmake.org/download/" rel="nofollow">CMake</a></strong> - Used to generate Visual Studio project files. Does not matter if either 32-bit or 64-bit version is installed.</li>
<li>
<strong><a href="https://web.archive.org/web/20240304183509/https://vulkan.lunarg.com/sdk/home#windows" rel="nofollow">Vulkan SDK</a></strong> - <strong>Make sure to select Latest SDK.</strong>
</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/e9b4203a1491c1c0d433b97c8d17e51144e34bdde05b8fb33b82a075872ce1af/68747470733a2f2f692e696d6775722e636f6d2f6769447775546d2e706e67" alt="2" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/giDwuTm.png"></p>
<ul>
<li>
<strong>Git</strong> - We recommend <a href="https://web.archive.org/web/20240304183509/https://gitforwindows.org/" rel="nofollow">Git for Windows</a>.</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/5071aa51bc44bb9c8ade83ce41607642bac7dc9c049f511ac823812df79e4c1e/68747470733a2f2f692e696d6775722e636f6d2f5565537a6b42772e706e67" alt="3" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/UeSzkBw.png"></p>
<ul>
<li>While installing Git Bash, you should tell it to include Git in your system path. (Choose the "Git from the command line and also from 3rd-party software" option.) If you missed that, don't worry, you'll just have to manually tell CMake where your git.exe is, since it's used to include version info into the built executable.</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/5bac078848b163baf8425aa33a7364a6859023861d05e024127f8be29ae29650/68747470733a2f2f692e696d6775722e636f6d2f783072527331742e706e67" alt="4" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/x0rRs1t.png"></p>
<div class="markdown-heading"><h3 class="heading-element">Cloning yuzu with Git</h3><a id="user-content-cloning-yuzu-with-git" class="anchor-element" aria-label="Permalink: Cloning yuzu with Git" href="#cloning-yuzu-with-git"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p><strong>Master:</strong></p>
<div class="highlight highlight-source-batchfile notranslate position-relative overflow-auto"><pre>git clone --recursive https://github.com/yuzu-emu/yuzu.git
<span class="pl-k">cd</span> yuzu</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone --recursive https://github.com/yuzu-emu/yuzu.git
cd yuzu" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Mainline (no assert):</strong></p>
<div class="highlight highlight-source-batchfile notranslate position-relative overflow-auto"><pre>git clone --recursive https://github.com/yuzu-emu/yuzu-mainline.git
<span class="pl-k">cd</span> yuzu-mainline</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone --recursive https://github.com/yuzu-emu/yuzu-mainline.git
cd yuzu-mainline" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/1f4381c1c994c1abf89d9c0808ef284bfb2193e33b8281b18ac08f84ceb5f31b/68747470733a2f2f692e696d6775722e636f6d2f436378494168742e706e67" alt="9" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/CcxIAht.png"></p>
<ul>
<li><em>(Note: yuzu by default downloads to <code>C:\Users\&lt;user-name&gt;\yuzu</code> (Master) or <code>C:\Users\&lt;user-name&gt;\yuzu-mainline</code> (Mainline)</em></li>
</ul>
<div class="markdown-heading"><h3 class="heading-element">Building</h3><a id="user-content-building" class="anchor-element" aria-label="Permalink: Building" href="#building"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li>
<p>Open the CMake GUI application and point it to the <code>yuzu</code> (Master) or <code>yuzu-mainline</code> (Mainline) directory.</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/6b5ee5ff3c5298e5f274cbdfe7fc781db9d11cc3f5684c1003a4bac9af1018a3/68747470733a2f2f692e696d6775722e636f6d2f714f736c4957762e706e67" alt="10" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/qOslIWv.png"></p>
</li>
<li>
<p>For the build directory, use a <code>/build</code> subdirectory inside the source directory or some other directory of your choice. (Tell CMake to create it.)</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://private-user-images.githubusercontent.com/20753089/246957039-738efcab-0da6-44ce-889d-becf3712db10.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDk1Nzc2MDksIm5iZiI6MTcwOTU3NzMwOSwicGF0aCI6Ii8yMDc1MzA4OS8yNDY5NTcwMzktNzM4ZWZjYWItMGRhNi00NGNlLTg4OWQtYmVjZjM3MTJkYjEwLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAzMDQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMzA0VDE4MzUwOVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTZhNWJiYmYyODNkYzE1ZWRjZGQzYTc2NWY3ZDM3MjQwNDUzMzg4NjA3NTA3NWFmYzU5ZDdiMTRkY2ZmZjMzZjcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.Q5IoPf4PptAMrRZUNah3Kdj-IXaEh9vjggTSr-0S_M4" alt="11" content-type-secured-asset="image/png"></p>
</li>
<li>
<p>Click the "Configure" button and choose <code>Visual Studio 17 2022</code>, with <code>x64</code> for the optional platform.</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/195da4d9b1a4dff76b77fe5a95b9dfd66479fb932ecb4653c0f9ca47267184a3/68747470733a2f2f692e696d6775722e636f6d2f444b695245614b2e706e67" alt="12" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/DKiREaK.png"></p>
<ul>
<li><em>(Note: If you used GitHub's own app to clone, run <code>git submodule update --init --recursive</code> to get the remaining dependencies)</em></li>
</ul>
</li>
<li>
<p>If you get an error about missing packages, enable <code>YUZU_USE_BUNDLED_VCPKG</code>, and then click Configure again.</p>
<ul>
<li><em>(You may also want to disable <code>YUZU_TESTS</code> in this case since Catch2 is not yet supported with this.)</em></li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/22451773/180585999-07316d6e-9751-4d11-b957-1cf57cd7cd58.png" alt="13"></p>
</li>
<li>
<p>Click "Generate" to create the project files.</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/2e25ff47cf5e54e53a0cac30cc256c98c1f97ec3f9c9e45b50dac89406329cf3/68747470733a2f2f692e696d6775722e636f6d2f354c4b6739326b2e706e67" alt="15" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/5LKg92k.png"></p>
</li>
<li>
<p>Open the solution file <code>yuzu.sln</code> in Visual Studio 2022, which is located in the build folder.</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/d914c4074c3bac7b8803d4cdd87a65f4f621d620599fcf143d79a5de8a5f640a/68747470733a2f2f692e696d6775722e636f6d2f323038794d6d6c2e706e67" alt="16" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/208yMml.png"></p>
</li>
<li>
<p>Depending if you want a graphical user interface or not (<code>yuzu</code> has the graphical user interface, while <code>yuzu-cmd</code> doesn't), select <code>yuzu</code> or <code>yuzu-cmd</code> in the Solution Explorer, right-click and <code>Set as StartUp Project</code>.</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/84e8c3a32f2d18817214aecdbddecf6e613b1d765bd9d337fce7920645d767da/68747470733a2f2f692e696d6775722e636f6d2f6e504d616a6e6e2e706e67" alt="17" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/nPMajnn.png">  <img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/3db18f7ae619b8e18b54332a0ad949c29bd6cb401a7d38011576453057cd98c8/68747470733a2f2f692e696d6775722e636f6d2f42444d4c7a525a2e706e67" alt="18" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/BDMLzRZ.png"></p>
</li>
<li>
<p>Select the appropriate build type, Debug for debug purposes or Release for performance (in case of doubt choose Release).</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/dde8f49e5fb9945036534748e89537fc3ebdcc78c492e170ffa8bd9d8b90d92e/68747470733a2f2f692e696d6775722e636f6d2f71786734726f432e706e67" alt="19" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/qxg4roC.png"></p>
</li>
<li>
<p>Right-click the project you want to build and press Build in the submenu or press F5.</p>
<p><img src="https://web.archive.org/web/20240304183509im_/https://camo.githubusercontent.com/c10e2425c124c2b8fc190286fd378a62910e4430338de07e7e5615cc769ea5a2/68747470733a2f2f692e696d6775722e636f6d2f436b51674f46572e706e67" alt="20" data-canonical-src="https://web.archive.org/web/20240304183509/https://i.imgur.com/CkQgOFW.png"></p>
</li>
</ul>
<p>Feel free to ask us in the IRC channel #yuzu-emu @ <a href="https://web.archive.org/web/20240304183509/https://web.libera.chat/" rel="nofollow">libera</a> or on <a href="https://web.archive.org/web/20240304183509/https://discord.com/invite/u77vRWY" rel="nofollow">Discord</a> if you have issues.</p>
<div class="markdown-heading"><h2 class="heading-element">Method II: MinGW-w64 Build with MSYS2</h2><a id="user-content-method-ii-mingw-w64-build-with-msys2" class="anchor-element" aria-label="Permalink: Method II: MinGW-w64 Build with MSYS2" href="#method-ii-mingw-w64-build-with-msys2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading"><h3 class="heading-element">Prerequisites to install</h3><a id="user-content-prerequisites-to-install" class="anchor-element" aria-label="Permalink: Prerequisites to install" href="#prerequisites-to-install"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li><a href="https://web.archive.org/web/20240304183509/https://www.msys2.org/" rel="nofollow">MSYS2</a></li>
<li>
<a href="https://web.archive.org/web/20240304183509/https://vulkan.lunarg.com/sdk/home#windows" rel="nofollow">Vulkan SDK</a> - <strong>Make sure to select Latest SDK.</strong>
</li>
<li>Make sure to follow the instructions and update to the latest version by running <code>pacman -Syu</code> as many times as needed.</li>
</ul>
<div class="markdown-heading"><h3 class="heading-element">Install yuzu dependencies for MinGW-w64</h3><a id="user-content-install-yuzu-dependencies-for-mingw-w64" class="anchor-element" aria-label="Permalink: Install yuzu dependencies for MinGW-w64" href="#install-yuzu-dependencies-for-mingw-w64"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li>Open the <code>MSYS2 MinGW 64-bit</code> (mingw64.exe) shell</li>
<li>Download and install all dependencies using: <code>pacman -Syu git make mingw-w64-x86_64-SDL2 mingw-w64-x86_64-cmake mingw-w64-x86_64-python-pip mingw-w64-x86_64-qt5 mingw-w64-x86_64-toolchain autoconf libtool automake-wrapper</code>
</li>
<li>Add MinGW binaries to the PATH: <code>echo 'PATH=/mingw64/bin:$PATH' &gt;&gt; ~/.bashrc</code>
</li>
<li>Add glslangValidator to the PATH: <code>echo 'PATH=$(readlink -e /c/VulkanSDK/*/Bin/):$PATH' &gt;&gt; ~/.bashrc</code>
</li>
</ul>
<div class="markdown-heading"><h3 class="heading-element">Clone the yuzu repository with Git</h3><a id="user-content-clone-the-yuzu-repository-with-git" class="anchor-element" aria-label="Permalink: Clone the yuzu repository with Git" href="#clone-the-yuzu-repository-with-git"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>git clone --recursive https://github.com/yuzu-emu/yuzu.git
<span class="pl-c1">cd</span> yuzu</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone --recursive https://github.com/yuzu-emu/yuzu.git
cd yuzu" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading"><h3 class="heading-element">Run the following commands to build yuzu (dynamically linked build)</h3><a id="user-content-run-the-following-commands-to-build-yuzu-dynamically-linked-build" class="anchor-element" aria-label="Permalink: Run the following commands to build yuzu (dynamically linked build)" href="#run-the-following-commands-to-build-yuzu-dynamically-linked-build"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>mkdir build <span class="pl-k">&amp;&amp;</span> <span class="pl-c1">cd</span> build
cmake -G <span class="pl-s"><span class="pl-pds">"</span>MSYS Makefiles<span class="pl-pds">"</span></span> -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF ..
make -j<span class="pl-s"><span class="pl-pds">$(</span>nproc<span class="pl-pds">)</span></span>
<span class="pl-c"><span class="pl-c">#</span> test yuzu out with</span>
./bin/yuzu.exe</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="mkdir build &amp;&amp; cd build
cmake -G &quot;MSYS Makefiles&quot; -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF ..
make -j$(nproc)
# test yuzu out with
./bin/yuzu.exe" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<ul>
<li><em>(Note: This build is not a static build meaning that you need to include all of the DLLs with the .exe in order to use it!)</em></li>
</ul>
<p>e.g.</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>cp externals/ffmpeg-<span class="pl-k">*</span>/bin/<span class="pl-k">*</span>.dll bin/</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cp externals/ffmpeg-*/bin/*.dll bin/" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Bonus Note: Running programs from inside <code>MSYS2 MinGW x64</code> shell has a different %PATH% than directly from explorer. This different %PATH% has the locations of the other DLLs required.
<img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/190571/165000848-005e8428-8a82-41b1-bb4d-4ce7797cdac8.png" alt="image"></p>
<div class="markdown-heading"><h3 class="heading-element">Building without Qt (Optional)</h3><a id="user-content-building-without-qt-optional" class="anchor-element" aria-label="Permalink: Building without Qt (Optional)" href="#building-without-qt-optional"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p>Doesn't require the rather large Qt dependency, but you will lack a GUI frontend:</p>
<ul>
<li>Pass the <code>-DENABLE_QT=no</code> flag to cmake</li>
</ul>
<div class="markdown-heading"><h2 class="heading-element">Method III: CLion Environment Setup</h2><a id="user-content-method-iii-clion-environment-setup" class="anchor-element" aria-label="Permalink: Method III: CLion Environment Setup" href="#method-iii-clion-environment-setup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading"><h3 class="heading-element">Minimal Dependencies</h3><a id="user-content-minimal-dependencies-1" class="anchor-element" aria-label="Permalink: Minimal Dependencies" href="#minimal-dependencies-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p>To build yuzu, you need to install the following:</p>
<ul>
<li>
<a href="https://web.archive.org/web/20240304183509/https://www.jetbrains.com/clion/" rel="nofollow">CLion</a> - This IDE is not free; for a free alternative, check Method I</li>
<li>
<a href="https://web.archive.org/web/20240304183509/https://vulkan.lunarg.com/sdk/home#windows" rel="nofollow">Vulkan SDK</a> - Make sure to select the Latest SDK.</li>
</ul>
<div class="markdown-heading"><h3 class="heading-element">Cloning yuzu with CLion</h3><a id="user-content-cloning-yuzu-with-clion" class="anchor-element" aria-label="Permalink: Cloning yuzu with CLion" href="#cloning-yuzu-with-clion"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li>Clone the Repository:</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899046-0d41d7d6-8e4d-4ed2-9587-b57088af5214.png" alt="1">
<img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899061-b2ea274a-e88c-40ae-bf0b-4450b46e9fea.png" alt="2">
<img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899076-0e5988c4-d431-4284-a5ff-9ecff973db76.png" alt="3"></p>
<div class="markdown-heading"><h3 class="heading-element">Building &amp; Setup</h3><a id="user-content-building--setup" class="anchor-element" aria-label="Permalink: Building &amp; Setup" href="#building--setup"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li>Once Cloned, You will be taken to a prompt like the image below:</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899092-3fe4cec6-a540-44e3-9e1e-3de9c2fffc2f.png" alt="4"></p>
<ul>
<li>Set the settings to the image below:</li>
<li>Change <code>Build type: Release</code>
</li>
<li>Change <code>Name: Release</code>
</li>
<li>Change <code>Toolchain Visual Studio</code>
</li>
<li>Change <code>Generator: Let CMake decide</code>
</li>
<li>Change <code>Build directory: build</code>
</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899164-6cee8482-3d59-428f-b1bc-e6dc793c9b20.png" alt="5"></p>
<ul>
<li>Click OK; now Clion will build a directory and index your code to allow for IntelliSense. Please be patient.</li>
<li>Once this process has been completed (No loading bar bottom right), you can now build yuzu</li>
<li>In the top right, click on the drop-down menu, select all configurations, then select yuzu</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899226-975048e9-bc6d-4ec1-bc2d-bd8a1e15ed04.png" alt="6"></p>
<ul>
<li>Now run by clicking the play button or pressing Shift+F10, and yuzu will auto-launch once built.</li>
</ul>
<p><img src="https://web.archive.org/web/20240304183509im_/https://user-images.githubusercontent.com/42481638/216899275-d514ec6a-e563-470e-81e2-3e04f0429b68.png" alt="7"></p>
<div class="markdown-heading"><h2 class="heading-element">Building from the command line with MSVC</h2><a id="user-content-building-from-the-command-line-with-msvc" class="anchor-element" aria-label="Permalink: Building from the command line with MSVC" href="#building-from-the-command-line-with-msvc"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-batchfile notranslate position-relative overflow-auto"><pre>git clone --recursive https://github.com/yuzu-emu/yuzu
<span class="pl-k">cd</span> yuzu
<span class="pl-k">mkdir</span> build
<span class="pl-k">cd</span> build
cmake .. -G <span class="pl-s"><span class="pl-pds">"</span>Visual Studio 17 2022<span class="pl-pds">"</span></span> -A x64
cmake --build . --config Release</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone --recursive https://github.com/yuzu-emu/yuzu
cd yuzu
mkdir build
cd build
cmake .. -G &quot;Visual Studio 17 2022&quot; -A x64
cmake --build . --config Release" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>

              </div>

          </div>
</div>
  <div style="min-width: 0" data-view-component="true" class="Layout-sidebar">          <div class="wiki-rightbar">
            <nav id="wiki-pages-box" class="mb-4 wiki-pages-box js-wiki-pages-box" aria-labelledby="wiki-pages-box-heading">
              
<div class="Box Box--condensed color-shadow-small">
  <div class="Box-header px-2 py-1 js-wiki-toggle-collapse" style="cursor: pointer">
    <h3 class="Box-title d-flex flex-items-center" id="wiki-pages-box-heading">
      <button id="icon-button-925ec210-69e0-4463-a5f4-bb3c5bf30f77" aria-labelledby="tooltip-c3994d55-17f6-4f8d-8609-987f84350407" type="button" data-view-component="true" class="Button Button--iconOnly Button--invisible Button--small js-wiki-sidebar-pages-toggle-chevron js-wiki-sidebar-pages-toggle-chevron-open">  <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down Button-visual">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
</button><tool-tip id="tooltip-c3994d55-17f6-4f8d-8609-987f84350407" for="icon-button-925ec210-69e0-4463-a5f4-bb3c5bf30f77" popover="manual" data-direction="s" data-type="label" data-view-component="true" class="sr-only position-absolute" aria-hidden="true" role="tooltip">Toggle tagle of contents</tool-tip>

      <span>Pages <span title="27" data-view-component="true" class="Counter Counter--primary">27</span></span>
    </h3>
  </div>
  <div class="d-none js-wiki-sidebar-toggle-display">
    <div class="filter-bar">
      <input type="text" id="wiki-pages-filter" class="form-control input-sm input-block js-filterable-field" placeholder="Find a page…" aria-label="Find a page…" autocomplete="off">
    </div>

    <ul class="m-0 p-0 list-style-none" data-filterable-for="wiki-pages-filter" data-filterable-type="substring" data-pjax="">
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki" data-view-component="true" class="Truncate-text text-bold py-1">Home</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Home/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/%5BDeprecated%5D-Building-Mesa-on-Arch-Linux" data-view-component="true" class="Truncate-text text-bold py-1">[Deprecated] Building Mesa on Arch Linux</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/%5BDeprecated%5D-Building-Mesa-on-Arch-Linux/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Bounties" data-view-component="true" class="Truncate-text text-bold py-1">Bounties</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Bounties/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Building-For-Android" data-view-component="true" class="Truncate-text text-bold py-1">Building For Android</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-For-Android/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Building-for-Linux" data-view-component="true" class="Truncate-text text-bold py-1">Building for Linux</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-for-Linux/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Building-for-macOS" data-view-component="true" class="Truncate-text text-bold py-1">Building for macOS</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-for-macOS/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Building-for-Windows" data-view-component="true" class="Truncate-text text-bold py-1">Building for Windows</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-for-Windows/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Contributing" data-view-component="true" class="Truncate-text text-bold py-1">Contributing</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Contributing/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Contributor-License-Agreement-Policy" data-view-component="true" class="Truncate-text text-bold py-1">Contributor License Agreement Policy</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Contributor-License-Agreement-Policy/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Developer-Information" data-view-component="true" class="Truncate-text text-bold py-1">Developer Information</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Developer-Information/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Dumping-Decryption-Keys-from-a-Switch-Console" data-view-component="true" class="Truncate-text text-bold py-1">Dumping Decryption Keys from a Switch Console</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Dumping-Decryption-Keys-from-a-Switch-Console/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Dumping-Game-Cartridges" data-view-component="true" class="Truncate-text text-bold py-1">Dumping Game Cartridges</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Dumping-Game-Cartridges/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Dumping-Installed-Titles" data-view-component="true" class="Truncate-text text-bold py-1">Dumping Installed Titles</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Dumping-Installed-Titles/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/FAQ" data-view-component="true" class="Truncate-text text-bold py-1">FAQ</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/FAQ/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/How-to-Install-and-Use-Game-Updates" data-view-component="true" class="Truncate-text text-bold py-1">How to Install and Use Game Updates</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/How-to-Install-and-Use-Game-Updates/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Open-Source-Page-for-testers" data-view-component="true" class="Truncate-text text-bold py-1">Open Source Page for testers</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Open-Source-Page-for-testers/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Overview-of-Switch-Game-Formats" data-view-component="true" class="Truncate-text text-bold py-1">Overview of Switch Game Formats</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Overview-of-Switch-Game-Formats/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Recommended-GPU-Drivers-for-Linux" data-view-component="true" class="Truncate-text text-bold py-1">Recommended GPU Drivers for Linux</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Recommended-GPU-Drivers-for-Linux/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Service-Function-Usage" data-view-component="true" class="Truncate-text text-bold py-1">Service Function Usage</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Service-Function-Usage/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Switch-Hardware-and-Software" data-view-component="true" class="Truncate-text text-bold py-1">Switch Hardware and Software</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Switch-Hardware-and-Software/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Switch-Homebrew" data-view-component="true" class="Truncate-text text-bold py-1">Switch Homebrew</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Switch-Homebrew/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods" data-view-component="true" class="Truncate-text text-bold py-1">Switch Mods</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Troubleshooting-Loader-Errors" data-view-component="true" class="Truncate-text text-bold py-1">Troubleshooting Loader Errors</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Troubleshooting-Loader-Errors/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Typical-Git-Workflow" data-view-component="true" class="Truncate-text text-bold py-1">Typical Git Workflow</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Typical-Git-Workflow/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/User-Directory" data-view-component="true" class="Truncate-text text-bold py-1">User Directory</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/User-Directory/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/Using-a-Controller-or-Android-Phone-for-Motion-or-Touch-Input" data-view-component="true" class="Truncate-text text-bold py-1">Using a Controller or Android Phone for Motion or Touch Input</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Using-a-Controller-or-Android-Phone-for-Motion-or-Touch-Input/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki/yuzu-Web-Service" data-view-component="true" class="Truncate-text text-bold py-1">yuzu Web Service</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/yuzu-Web-Service/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages-link">
            <button type="button" data-view-component="true" class="Link--muted js-wiki-more-pages-link btn-link mx-auto f6">    Show 12 more pages…
</button>        </li>
    </ul>
  </div>
</div>

            </nav>

              <div class="gollum-markdown-content">
                <div class="Box Box--condensed mb-4">
                  <div class="Box-body wiki-custom-sidebar markdown-body">
                    <div class="markdown-heading"><h2 class="heading-element"><a href="https://web.archive.org/web/20240304183509/https://github.com/yuzu-emu/yuzu/wiki">Home</a></h2><a id="user-content-home" class="anchor-element" aria-label="Permalink: Home" href="#home"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li>
<strong>Users:</strong>
<ul>
<li><a href="https://web.archive.org/web/20240304183509/https://yuzu-emu.org/help/quickstart/" rel="nofollow">Quickstart guide</a></li>
<li><a href="wiki/FAQ">FAQ</a></li>
<li><a href="wiki/Overview-of-Switch-Game-Formats">Overview of Switch Game Formats</a></li>
<li><a href="wiki/User-Directory">User Directory</a></li>
<li><a href="https://web.archive.org/web/20240304183509/https://yuzu-emu.org/help/early-access/" rel="nofollow">yuzu Early Access</a></li>
<li><a href="wiki/yuzu-Web-Service">yuzu Web Service</a></li>
<li><a href="https://web.archive.org/web/20240304183509/https://yuzu-emu.org/help/feature/telemetry/" rel="nofollow">Telemetry</a></li>
<li><a href="https://web.archive.org/web/20240304183509/https://yuzu-emu.org/help/feature/boxcat/" rel="nofollow">Boxcat</a></li>
<li><a href="wiki/Recommended-GPU-Drivers-for-Linux">Recommended GPU Drivers for Linux</a></li>
</ul>
</li>
</ul>
<h1></h1>
<ul>
<li>
<strong>General:</strong>
<ul>
<li><a href="wiki/Contributing">Contributing</a></li>
<li><a href="https://web.archive.org/web/20240304183509/https://yuzu-emu.org/bounties/" rel="nofollow">Bounties</a></li>
</ul>
</li>
</ul>
<hr>
<ul>
<li>
<strong><a href="wiki/Developer-Information">Developers</a>:</strong>
<ul>
<li>Building yuzu:
<ul>
<li><a href="wiki/Building-for-Windows">Windows</a></li>
<li><a href="wiki/Building-for-Linux">Linux</a></li>
<li><a href="wiki/Building-for-Android">Android</a></li>
<li><a href="wiki/Building-for-macOS">macOS</a></li>
</ul>
</li>
<li><a href="wiki/Switch-Hardware-and-Software">Switch Hardware and Software Documentation</a></li>
<li><a href="wiki/Switch-Homebrew">Switch Homebrew and Libraries</a></li>
<li><a href="wiki/Service-Function-Usage">Service Function Usage</a></li>
<li>
<a href="wiki/Contributing#contributing">Contributing</a>
<ul>
<li>
<a href="https://web.archive.org/web/20240304183509/https://cla-assistant.io/yuzu-emu/yuzu" rel="nofollow">Contributor License Agreement</a>
<ul>
<li><a href="wiki/Contributor-License-Agreement-Policy">Policy</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="wiki/Typical-Git-Workflow">Typical Git workflow</a></li>
</ul>
</li>
</ul>

                  </div>
                </div>
              </div>

            <h5 class="mt-0 mb-2">Clone this wiki locally</h5>
            <div class="width-full input-group">
              <input id="wiki-clone-url" type="text" data-autoselect="" class="form-control input-sm text-small color-fg-muted input-monospace" aria-label="Clone URL for this wiki" value="https://github.com/yuzu-emu/yuzu.wiki.git" readonly="">
              <span class="input-group-button">
                <clipboard-copy for="wiki-clone-url" aria-label="Copy to clipboard" data-view-component="true" class="btn btn-sm zeroclipboard-button" tabindex="0" role="button">
    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
    <svg style="display: none;" aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check color-fg-success">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
</clipboard-copy>
              </span>
            </div>
          </div>
</div>
  
</div>    </div>
  
* __Linux__: 

<div id="wiki-content" class="mt-4">
      <div data-view-component="true" class="Layout Layout--flowRow-until-md Layout--sidebarPosition-end Layout--sidebarPosition-flowRow-end">
  <div data-view-component="true" class="Layout-main">          <div id="wiki-body" class="gollum-markdown-content">
              <div class="markdown-body">
                <p><strong>This article was written for developers. Users looking to simply run yuzu should try downloading <a href="https://web.archive.org/web/20240304183515/https://yuzu-emu.org/downloads/" rel="nofollow">Mainline</a> first. As it is an AppImage, it only needs to be downloaded and made executable to use it.</strong></p>
<hr>
<div class="markdown-heading"><h3 class="heading-element">Dependencies</h3><a id="user-content-dependencies" class="anchor-element" aria-label="Permalink: Dependencies" href="#dependencies"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p>You'll need to download and install the following to build yuzu:</p>
<ul>
<li>
<a href="https://web.archive.org/web/20240304183515/https://gcc.gnu.org/" rel="nofollow">GCC</a> v11+ (for C++20 support) &amp; misc
<ul>
<li>This page is being updated as we transition to GCC 11</li>
</ul>
</li>
<li>If GCC 12 is installed, <a href="https://web.archive.org/web/20240304183515/https://clang.llvm.org/" rel="nofollow">Clang</a> v14+ is required for compiling</li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://www.cmake.org/" rel="nofollow">CMake</a> 3.15+</li>
</ul>
<p>The following are handled by yuzu's externals:</p>
<ul>
<li><a href="https://web.archive.org/web/20240304183515/https://ffmpeg.org/" rel="nofollow">FFmpeg</a></li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://www.libsdl.org/download-2.0.php" rel="nofollow">SDL2</a> 2.0.18+</li>
<li><a href="https://web.archive.org/web/20240304183515/https://opus-codec.org/downloads/" rel="nofollow">opus</a></li>
</ul>
<p>If version 5.15.2 is not already installed, pre-compiled binaries for Qt 5.15.2 will be downloaded from <a href="https://web.archive.org/web/20240304183515/https://github.com/yuzu-emu/ext-linux-bin">here</a> automatically by CMake:</p>
<ul>
<li>
<a href="https://web.archive.org/web/20240304183515/https://qt-project.org/downloads" rel="nofollow">Qt</a> 5.15+</li>
</ul>
<p>All other dependencies will be downloaded by <a href="https://web.archive.org/web/20240304183515/https://vcpkg.io/" rel="nofollow">vcpkg</a> if needed:</p>
<ul>
<li>
<a href="https://web.archive.org/web/20240304183515/https://www.boost.org/users/download/" rel="nofollow">Boost</a> 1.79.0+</li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://github.com/catchorg/Catch2">Catch2</a> 2.13.7 - 2.13.9</li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://fmt.dev/" rel="nofollow">fmt</a> 8.0.1+</li>
<li>
<a href="https://web.archive.org/web/20240304183515/http://www.lz4.org/" rel="nofollow">lz4</a> 1.8+</li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://github.com/nlohmann/json">nlohmann_json</a> 3.8+</li>
<li><a href="https://web.archive.org/web/20240304183515/https://www.openssl.org/source/" rel="nofollow">OpenSSL</a></li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://www.zlib.net/" rel="nofollow">ZLIB</a> 1.2+</li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://facebook.github.io/zstd/" rel="nofollow">zstd</a> 1.5+</li>
</ul>
<p>If an ARM64 build is intended, export <code>VCPKG_FORCE_SYSTEM_BINARIES=1</code>.</p>
<p>Dependencies are listed here as commands that can be copied/pasted. Of course, they should be inspected before being run.</p>
<ul>
<li>Arch / Manjaro:
<ul>
<li><code>sudo pacman -Syu --needed base-devel boost catch2 cmake ffmpeg fmt git glslang libzip lz4 mbedtls ninja nlohmann-json openssl opus qt5 sdl2 zlib zstd zip unzip</code></li>
<li>Building with QT Web Engine needs to be specified when running CMake with the param <code>-DCMAKE_CXX_FLAGS="-I/usr/include/qt/QtWebEngineWidgets"</code> with qt5-webengine installed.</li>
<li>GCC 11 or later is required.</li>
</ul>
</li>
<li>Ubuntu / Linux Mint / Debian:
<ul>
<li><code>sudo apt-get install autoconf cmake g++-11 gcc-11 git glslang-tools libasound2 libboost-context-dev libglu1-mesa-dev libhidapi-dev libpulse-dev libtool libudev-dev libxcb-icccm4 libxcb-image0 libxcb-keysyms1 libxcb-render-util0 libxcb-xinerama0 libxcb-xkb1 libxext-dev libxkbcommon-x11-0 mesa-common-dev nasm ninja-build qtbase5-dev qtbase5-private-dev qtwebengine5-dev qtmultimedia5-dev libmbedtls-dev catch2 libfmt-dev liblz4-dev nlohmann-json3-dev libzstd-dev libssl-dev libavfilter-dev libavcodec-dev libswscale-dev</code></li>
<li>Ubuntu 22.04, Linux Mint 20, or Debian Bullseye or later is required.</li>
<li>Users need to manually specify building with QT Web Engine enabled.  This is done using the parameter <code>-DYUZU_USE_QT_WEB_ENGINE=ON</code> when running CMake.</li>
<li>Users need to manually specify building with GCC 11. This can be done by adding the parameters <code>-DCMAKE_C_COMPILER=gcc-11 -DCMAKE_CXX_COMPILER=g++-11</code> when running CMake. i.e.</li>
<li>Users need to manually disable building SDL2 from externals if they intend to use the version provided by their system by adding the parameters <code>-DYUZU_USE_EXTERNAL_SDL2=OFF</code>
</li>
</ul>
</li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>git submodule update --init --recursive
cmake .. -GNinja -DCMAKE_C_COMPILER=gcc-11 -DCMAKE_CXX_COMPILER=g++-11
</code></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git submodule update --init --recursive
cmake .. -GNinja -DCMAKE_C_COMPILER=gcc-11 -DCMAKE_CXX_COMPILER=g++-11" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<ul>
<li>Fedora:
<ul>
<li><code>sudo dnf install autoconf ccache cmake fmt-devel gcc{,-c++} glslang hidapi-devel json-devel libtool libusb1-devel libzstd-devel lz4-devel nasm ninja-build openssl-devel pulseaudio-libs-devel qt5-linguist qt5-qtbase{-private,}-devel qt5-qtwebengine-devel qt5-qtmultimedia-devel speexdsp-devel wayland-devel zlib-devel ffmpeg-devel libXext-devel</code></li>
<li>Fedora 32 or later is required.</li>
<li>Due to GCC 12, Fedora 36 or later users need to install <code>clang</code>, and configure CMake to use it via <code>-DCMAKE_CXX_COMPILER=clang++ -DCMAKE_C_COMPILER=clang</code>
</li>
<li>CMake arguments to force system libraries:
<ul>
<li>SDL2: <code>-DYUZU_USE_BUNDLED_SDL2=OFF -DYUZU_USE_EXTERNAL_SDL2=OFF</code>
</li>
<li>FFmpeg: <code>-DYUZU_USE_EXTERNAL_FFMPEG=OFF</code>
</li>
</ul>
</li>
<li>
<a href="https://web.archive.org/web/20240304183515/https://rpmfusion.org/" rel="nofollow">RPM Fusion</a> (free) is required to install <code>ffmpeg-devel</code>
</li>
</ul>
</li>
<li>Gentoo:
<ul>
<li>
<strong>**Disclaimer**</strong>: this dependency list was written by a novice Gentoo user who first set it up with a DE, and then based this list off of the Fedora dependency list. This may be missing some requirements, or includes too many. Caveat emptor.</li>
<li><code>emerge --ask app-arch/lz4 dev-libs/boost dev-libs/hidapi dev-libs/libzip dev-libs/openssl dev-qt/linguist dev-qt/qtconcurrent dev-qt/qtcore dev-util/cmake dev-util/glslang dev-vcs/git media-libs/alsa-lib media-libs/opus media-sound/pulseaudio media-video/ffmpeg net-libs/mbedtls sys-libs/zlib x11-libs/libXext</code></li>
<li>GCC 11 or later is required.</li>
<li>Users may need to append <code>pulseaudio</code>, <code>bindist</code> and <code>context</code> to the <code>USE</code> flag.</li>
</ul>
</li>
</ul>
<div class="markdown-heading"><h3 class="heading-element">Cloning yuzu with Git</h3><a id="user-content-cloning-yuzu-with-git" class="anchor-element" aria-label="Permalink: Cloning yuzu with Git" href="#cloning-yuzu-with-git"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p><strong>Master:</strong></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>git clone --recursive https://github.com/yuzu-emu/yuzu
<span class="pl-c1">cd</span> yuzu</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone --recursive https://github.com/yuzu-emu/yuzu
cd yuzu" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p><strong>Mainline:</strong></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>git clone --recursive https://github.com/yuzu-emu/yuzu-mainline
<span class="pl-c1">cd</span> yuzu-mainline</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone --recursive https://github.com/yuzu-emu/yuzu-mainline
cd yuzu-mainline" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>The <code>--recursive</code> option automatically clones the required Git submodules.</p>
<div class="markdown-heading"><h3 class="heading-element">Building yuzu in Release Mode (Optimized)</h3><a id="user-content-building-yuzu-in-release-mode-optimized" class="anchor-element" aria-label="Permalink: Building yuzu in Release Mode (Optimized)" href="#building-yuzu-in-release-mode-optimized"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p>If you need to run ctests, you can disable <code>-DYUZU_TESTS=OFF</code> and install Catch2.</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>mkdir build <span class="pl-k">&amp;&amp;</span> <span class="pl-c1">cd</span> build
cmake .. -GNinja -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF
ninja
sudo ninja install </pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="mkdir build &amp;&amp; cd build
cmake .. -GNinja -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF
ninja
sudo ninja install " tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p>Optionally, you can use <code>cmake-gui ..</code> to adjust various options (e.g. disable the Qt GUI).</p>
<div class="markdown-heading"><h3 class="heading-element">Building yuzu in Debug Mode (Slow)</h3><a id="user-content-building-yuzu-in-debug-mode-slow" class="anchor-element" aria-label="Permalink: Building yuzu in Debug Mode (Slow)" href="#building-yuzu-in-debug-mode-slow"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>mkdir build <span class="pl-k">&amp;&amp;</span> <span class="pl-c1">cd</span> build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=Debug -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF
ninja</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="mkdir build &amp;&amp; cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=Debug -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF
ninja" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading"><h3 class="heading-element">Building with debug symbols</h3><a id="user-content-building-with-debug-symbols" class="anchor-element" aria-label="Permalink: Building with debug symbols" href="#building-with-debug-symbols"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre>mkdir build <span class="pl-k">&amp;&amp;</span> <span class="pl-c1">cd</span> build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=RelWithDebInfo -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF
ninja</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="mkdir build &amp;&amp; cd build
cmake .. -GNinja -DCMAKE_BUILD_TYPE=RelWithDebInfo -DYUZU_USE_BUNDLED_VCPKG=ON -DYUZU_TESTS=OFF
ninja" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading"><h3 class="heading-element">Running without installing</h3><a id="user-content-running-without-installing" class="anchor-element" aria-label="Permalink: Running without installing" href="#running-without-installing"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p>After building, the binaries <code>yuzu</code> and <code>yuzu-cmd</code> (depending on your build options) will end up in <code>build/bin/</code>.</p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre><span class="pl-c"><span class="pl-c">#</span> SDL</span>
<span class="pl-c1">cd</span> build/bin/
./yuzu-cmd

<span class="pl-c"><span class="pl-c">#</span> Qt</span>
<span class="pl-c1">cd</span> build/bin/
./yuzu</pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="# SDL
cd build/bin/
./yuzu-cmd

# Qt
cd build/bin/
./yuzu" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading"><h3 class="heading-element">Debugging</h3><a id="user-content-debugging" class="anchor-element" aria-label="Permalink: Debugging" href="#debugging"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ol>
<li>Enable CPU debugging
<img src="https://web.archive.org/web/20240304183515im_/https://raw.githubusercontent.com/flathub/org.yuzu_emu.yuzu/master/assets/yuzu-settings-2.png" alt="">
</li>
<li>Disable both Host MMU emulation options
<img src="https://web.archive.org/web/20240304183515im_/https://raw.githubusercontent.com/flathub/org.yuzu_emu.yuzu/master/assets/yuzu-settings-1.png" alt="">
</li>
<li>Run gdb</li>
</ol>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto"><pre><span class="pl-c1">cd</span> data
gdb ../build/bin/yuzu            <span class="pl-c"><span class="pl-c">#</span> Start GDB</span>
(gdb) run                        <span class="pl-c"><span class="pl-c">#</span> Run yuzu under GDB</span>
<span class="pl-k">&lt;</span>crash<span class="pl-k">&gt;</span>
(gdb) bt                         <span class="pl-c"><span class="pl-c">#</span> Print a backtrace of the entire callstack to see which codepath the crash occurred on</span></pre><div class="zeroclipboard-container position-absolute right-0 top-0">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn js-clipboard-copy m-2 p-0 tooltipped-no-delay" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd data
gdb ../build/bin/yuzu            # Start GDB
(gdb) run                        # Run yuzu under GDB
<crash>
(gdb) bt                         # Print a backtrace of the entire callstack to see which codepath the crash occurred on" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon m-2">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none m-2">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>

              </div>

          </div>
</div>
  <div style="min-width: 0" data-view-component="true" class="Layout-sidebar">          <div class="wiki-rightbar">
            <nav id="wiki-pages-box" class="mb-4 wiki-pages-box js-wiki-pages-box" aria-labelledby="wiki-pages-box-heading">
              
<div class="Box Box--condensed color-shadow-small">
  <div class="Box-header px-2 py-1 js-wiki-toggle-collapse" style="cursor: pointer">
    <h3 class="Box-title d-flex flex-items-center" id="wiki-pages-box-heading">
      <button id="icon-button-52a763b9-e52f-4686-8506-8da61a2f6fa6" aria-labelledby="tooltip-c3ba4e9d-9dd0-425f-b456-6bf877083061" type="button" data-view-component="true" class="Button Button--iconOnly Button--invisible Button--small js-wiki-sidebar-pages-toggle-chevron js-wiki-sidebar-pages-toggle-chevron-open">  <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down Button-visual">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
</button><tool-tip id="tooltip-c3ba4e9d-9dd0-425f-b456-6bf877083061" for="icon-button-52a763b9-e52f-4686-8506-8da61a2f6fa6" popover="manual" data-direction="s" data-type="label" data-view-component="true" class="sr-only position-absolute" aria-hidden="true" role="tooltip">Toggle tagle of contents</tool-tip>

      <span>Pages <span title="27" data-view-component="true" class="Counter Counter--primary">27</span></span>
    </h3>
  </div>
  <div class="d-none js-wiki-sidebar-toggle-display">
    <div class="filter-bar">
      <input type="text" id="wiki-pages-filter" class="form-control input-sm input-block js-filterable-field" placeholder="Find a page…" aria-label="Find a page…" autocomplete="off">
    </div>

    <ul class="m-0 p-0 list-style-none" data-filterable-for="wiki-pages-filter" data-filterable-type="substring" data-pjax="">
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki" data-view-component="true" class="Truncate-text text-bold py-1">Home</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Home/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/%5BDeprecated%5D-Building-Mesa-on-Arch-Linux" data-view-component="true" class="Truncate-text text-bold py-1">[Deprecated] Building Mesa on Arch Linux</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/%5BDeprecated%5D-Building-Mesa-on-Arch-Linux/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Bounties" data-view-component="true" class="Truncate-text text-bold py-1">Bounties</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Bounties/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Building-For-Android" data-view-component="true" class="Truncate-text text-bold py-1">Building For Android</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-For-Android/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Building-for-Linux" data-view-component="true" class="Truncate-text text-bold py-1">Building for Linux</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-for-Linux/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Building-for-macOS" data-view-component="true" class="Truncate-text text-bold py-1">Building for macOS</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-for-macOS/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Building-for-Windows" data-view-component="true" class="Truncate-text text-bold py-1">Building for Windows</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Building-for-Windows/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Contributing" data-view-component="true" class="Truncate-text text-bold py-1">Contributing</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Contributing/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Contributor-License-Agreement-Policy" data-view-component="true" class="Truncate-text text-bold py-1">Contributor License Agreement Policy</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Contributor-License-Agreement-Policy/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Developer-Information" data-view-component="true" class="Truncate-text text-bold py-1">Developer Information</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Developer-Information/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Dumping-Decryption-Keys-from-a-Switch-Console" data-view-component="true" class="Truncate-text text-bold py-1">Dumping Decryption Keys from a Switch Console</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Dumping-Decryption-Keys-from-a-Switch-Console/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Dumping-Game-Cartridges" data-view-component="true" class="Truncate-text text-bold py-1">Dumping Game Cartridges</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Dumping-Game-Cartridges/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Dumping-Installed-Titles" data-view-component="true" class="Truncate-text text-bold py-1">Dumping Installed Titles</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Dumping-Installed-Titles/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/FAQ" data-view-component="true" class="Truncate-text text-bold py-1">FAQ</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/FAQ/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/How-to-Install-and-Use-Game-Updates" data-view-component="true" class="Truncate-text text-bold py-1">How to Install and Use Game Updates</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/How-to-Install-and-Use-Game-Updates/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Open-Source-Page-for-testers" data-view-component="true" class="Truncate-text text-bold py-1">Open Source Page for testers</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Open-Source-Page-for-testers/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Overview-of-Switch-Game-Formats" data-view-component="true" class="Truncate-text text-bold py-1">Overview of Switch Game Formats</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Overview-of-Switch-Game-Formats/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Recommended-GPU-Drivers-for-Linux" data-view-component="true" class="Truncate-text text-bold py-1">Recommended GPU Drivers for Linux</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Recommended-GPU-Drivers-for-Linux/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Service-Function-Usage" data-view-component="true" class="Truncate-text text-bold py-1">Service Function Usage</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Service-Function-Usage/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Switch-Hardware-and-Software" data-view-component="true" class="Truncate-text text-bold py-1">Switch Hardware and Software</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Switch-Hardware-and-Software/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Switch-Homebrew" data-view-component="true" class="Truncate-text text-bold py-1">Switch Homebrew</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Switch-Homebrew/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods" data-view-component="true" class="Truncate-text text-bold py-1">Switch Mods</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Switch-Mods/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Troubleshooting-Loader-Errors" data-view-component="true" class="Truncate-text text-bold py-1">Troubleshooting Loader Errors</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Troubleshooting-Loader-Errors/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Typical-Git-Workflow" data-view-component="true" class="Truncate-text text-bold py-1">Typical Git Workflow</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Typical-Git-Workflow/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/User-Directory" data-view-component="true" class="Truncate-text text-bold py-1">User Directory</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/User-Directory/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/Using-a-Controller-or-Android-Phone-for-Motion-or-Touch-Input" data-view-component="true" class="Truncate-text text-bold py-1">Using a Controller or Android Phone for Motion or Touch Input</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/Using-a-Controller-or-Android-Phone-for-Motion-or-Touch-Input/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages px-2 py-2">
          <details class="details-reset">
  <summary>
    <div class="d-flex flex-items-start">
      <div class="p-2 mt-n1 mb-n1 ml-n1 btn btn-octicon js-wiki-sidebar-toc-toggle-chevron-button ">
        <svg hidden="hidden" style="box-sizing: content-box; color: var(--color-icon-primary);" width="16" height="16" viewBox="0 0 16 16" fill="none" data-view-component="true" class="js-wiki-sidebar-toc-spinner mr-0 v-align-text-bottom anim-rotate">
  <circle cx="8" cy="8" r="7" stroke="currentColor" stroke-opacity="0.25" stroke-width="2" vector-effect="non-scaling-stroke" fill="none"></circle>
  <path d="M15 8a7.002 7.002 0 00-7-7" stroke="currentColor" stroke-width="2" stroke-linecap="round" vector-effect="non-scaling-stroke"></path>
</svg>
        <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-triangle-down js-wiki-sidebar-toc-toggle-chevron mr-0">
    <path d="m4.427 7.427 3.396 3.396a.25.25 0 0 0 .354 0l3.396-3.396A.25.25 0 0 0 11.396 7H4.604a.25.25 0 0 0-.177.427Z"></path>
</svg>
      </div>
      <span data-view-component="true" class="Truncate">
    <a href="/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki/yuzu-Web-Service" data-view-component="true" class="Truncate-text text-bold py-1">yuzu Web Service</a>
</span>    </div>
  </summary>

    <include-fragment class="js-wiki-sidebar-toc-fragment" loading="lazy" src="https://github.com/yuzu-emu/yuzu/wiki/yuzu-Web-Service/_toc">
    </include-fragment>
</details>

        </li>
        <li class="Box-row wiki-more-pages-link">
            <button type="button" data-view-component="true" class="Link--muted js-wiki-more-pages-link btn-link mx-auto f6">    Show 12 more pages…
</button>        </li>
    </ul>
  </div>
</div>

            </nav>

              <div class="gollum-markdown-content">
                <div class="Box Box--condensed mb-4">
                  <div class="Box-body wiki-custom-sidebar markdown-body">
                    <div class="markdown-heading"><h2 class="heading-element"><a href="https://web.archive.org/web/20240304183515/https://github.com/yuzu-emu/yuzu/wiki">Home</a></h2><a id="user-content-home" class="anchor-element" aria-label="Permalink: Home" href="#home"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul>
<li>
<strong>Users:</strong>
<ul>
<li><a href="https://web.archive.org/web/20240304183515/https://yuzu-emu.org/help/quickstart/" rel="nofollow">Quickstart guide</a></li>
<li><a href="wiki/FAQ">FAQ</a></li>
<li><a href="wiki/Overview-of-Switch-Game-Formats">Overview of Switch Game Formats</a></li>
<li><a href="wiki/User-Directory">User Directory</a></li>
<li><a href="https://web.archive.org/web/20240304183515/https://yuzu-emu.org/help/early-access/" rel="nofollow">yuzu Early Access</a></li>
<li><a href="wiki/yuzu-Web-Service">yuzu Web Service</a></li>
<li><a href="https://web.archive.org/web/20240304183515/https://yuzu-emu.org/help/feature/telemetry/" rel="nofollow">Telemetry</a></li>
<li><a href="https://web.archive.org/web/20240304183515/https://yuzu-emu.org/help/feature/boxcat/" rel="nofollow">Boxcat</a></li>
<li><a href="wiki/Recommended-GPU-Drivers-for-Linux">Recommended GPU Drivers for Linux</a></li>
</ul>
</li>
</ul>
<h1></h1>
<ul>
<li>
<strong>General:</strong>
<ul>
<li><a href="wiki/Contributing">Contributing</a></li>
<li><a href="https://web.archive.org/web/20240304183515/https://yuzu-emu.org/bounties/" rel="nofollow">Bounties</a></li>
</ul>
</li>
</ul>
<hr>
<ul>
<li>
<strong><a href="wiki/Developer-Information">Developers</a>:</strong>
<ul>
<li>Building yuzu:
<ul>
<li><a href="wiki/Building-for-Windows">Windows</a></li>
<li><a href="wiki/Building-for-Linux">Linux</a></li>
<li><a href="wiki/Building-for-Android">Android</a></li>
<li><a href="wiki/Building-for-macOS">macOS</a></li>
</ul>
</li>
<li><a href="wiki/Switch-Hardware-and-Software">Switch Hardware and Software Documentation</a></li>
<li><a href="wiki/Switch-Homebrew">Switch Homebrew and Libraries</a></li>
<li><a href="wiki/Service-Function-Usage">Service Function Usage</a></li>
<li>
<a href="wiki/Contributing#contributing">Contributing</a>
<ul>
<li>
<a href="https://web.archive.org/web/20240304183515/https://cla-assistant.io/yuzu-emu/yuzu" rel="nofollow">Contributor License Agreement</a>
<ul>
<li><a href="wiki/Contributor-License-Agreement-Policy">Policy</a></li>
</ul>
</li>
</ul>
</li>
<li><a href="wiki/Typical-Git-Workflow">Typical Git workflow</a></li>
</ul>
</li>
</ul>

                  </div>
                </div>
              </div>

            <h5 class="mt-0 mb-2">Clone this wiki locally</h5>
            <div class="width-full input-group">
              <input id="wiki-clone-url" type="text" data-autoselect="" class="form-control input-sm text-small color-fg-muted input-monospace" aria-label="Clone URL for this wiki" value="https://github.com/yuzu-emu/yuzu.wiki.git" readonly="">
              <span class="input-group-button">
                <clipboard-copy for="wiki-clone-url" aria-label="Copy to clipboard" data-view-component="true" class="btn btn-sm zeroclipboard-button" tabindex="0" role="button">
    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
    <svg style="display: none;" aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check color-fg-success">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
</clipboard-copy>
              </span>
            </div>
          </div>
</div>
  
</div>    </div>

## Download

## License

yuzu is licensed under the GPLv3 (or any later version).
