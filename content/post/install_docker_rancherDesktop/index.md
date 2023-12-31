---
title: "Install Docker rancher Desktop" # Title of the blog post.
date: 2023-12-31T07:41:33+05:30 # Date of post creation.
description: "Article description." # Description used for search engine.
featured: false # Sets if post is a featured post, making appear on the home page side bar.
draft: false # Sets whether to render this page. Draft of true will not be rendered.
showShare: false
toc: false # Controls if a table of contents should be generated for first-level links automatically.
# menu: main
usePageBundles: true # Set to true to group assets like images in the same folder as this post.
featureImage: "introduction_preferences_tabKubernetes.png" # Sets featured image on blog post.
featureImageAlt: 'Rancher Interface' # Alternative text for featured image.
featureImageCap: 'The above image shows Kubernetes settings on Mac on the left and Windows on the right.' # Caption (optional).
thumbnail: "rancher_desktop_logo.png" # Sets thumbnail image appearing inside card on homepage.
shareImage: "/images/path/share.png" # Designate a separate image for social media sharing.
codeMaxLines: 10 # Override global value for how many lines within a code block before auto-collapsing.
codeLineNumbers: false # Override global value for showing of line numbers within code block.
figurePositionShow: true # Override global value for showing the figure label.
categories:
  - DevOps
tags:
  - Docker
  - tools
# comment: false # Disable comment if false.
---
# Installation
Rancher Desktop is deliverd as a desktop application. You can download it from the [release page on GitHub](https://github.com/rancher-sandbox/rancher-desktop/releases).

When run for the first time or when changing versions, kubernetes containers images are downloaded. It may take a little time to load on first run for a new Kubernetes version.

# MacOS
## Requirements
Rancher Desktop requires the following on macOS:
- macOS Catalina 10.15 or higer.
- Apple Silicon (M1) or Intel CPU with VT-x.
- Persistent internet connection.

It is also recommended to have:
- 8 GB of memory
- 4 CPU

Additional resources may be required depending on the workloads you plan to run.

## Installing Rancher Desktop on macOS
1. Go to the [release page](https://github.com/rancher-sandbox/rancher-desktop/releases) on GitHub.
2. Find the version of Rancher Desktop you want to download.
3. Expand the **Assets** section and download `Rancher.Desktop-X.Y.Z.dmg`, where `X.Y.Z` is the version of Rancher Desktop.
4. Navigate to the directory where you downloaded the installer to and run the installer. This will usually be the `Downloads` folder.
5. Double-click the DMG file.
6. In the Finder window that opens, drag the Rancher Desktop icon to the Applications folder.
7. Navigate to the `Applications` folder and double-click the Rancher Desktop to launch it.

## Uninstalling Racher Desktop on macOS
1. Open **Finder > Applications**.
2. Find Rancher Desktop.
3. Select it and choose **File > Move to Trash**.
4. To delete the app, Finder > Empty Trash.

# Windows
## Requirements
Rancher Desktop requires the following on Windows:
- Windows 10 build 1909 or higher. The home edition is supported.
- Running on a machine with virtualization capabilities.
- Persistent internet connection.

Rancher Desktop requires Windows Subsystem for Linux (WSL) on windows, this will automatically be installed as part of the Rancher Desktop setup. Manually downloading a distribution is not necessary.

It is also recommended to have:
- 8 GB of memory
- 4 CPU

Additional resources may be required depending on workloads you plan to run.

## Installing Rancher Desktop on Windows
1. Go to the [release page](https://github.com/rancher-sandbox/rancher-desktop/releases) on GitHub.
2. Find the version of Rancher Desktop you want to download.
3. Expand the **Assets** section and download the Windows installer. It will be called `Rancher.Desktop.Setup.X.Y.Z.msi`, where `X.Y.Z` is the version of Rancher Desktop.
4. Navigate to the directory where you downloaded the installer to and run the installer. This will usually be the `Downloads` folder.
5. Review the License Agreement and click **I Agree** to proceed with the installation.
6. If prompted, choose between installing for everyone on the machine or installing just for the current user. Installing for everyone is preferred in order to install the Rancher Desktop Privileged service.
7. Follow the prompts to confirm installation.
8. When the installation completes, click **Finish** to close the installation wizard.

## Uninstalling Rancher Desktop on Windows
1. From the taskbar, click the **Start** menu.
2. Go to **Settings > Apps > Apps & features**.
3. Find and select the Rancher Desktop entry.
4. Click on **Uninstall** and click it again when the confirmation appears.
5. Follow the prompts on the Rancher Desktop uninstaller to proceed.
6. Click **Finish** when complete.