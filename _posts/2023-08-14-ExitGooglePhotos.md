---
layout: post
title: "Exit Google Photos"
categories: tech
author: 
- Robert Triggs
---

[https://www.androidauthority.com/immich-google-photos-alternative-3353286/](https://www.androidauthority.com/immich-google-photos-alternative-3353286/) 

I tried a self-hosted Google Photos alternative but still can't switch
Cloud convenience still trumps self-hosted control, for now.



***Immich photo app gallery***
Cutting the cloud tether is increasingly easy, with plenty of excellent self-hosted options to house your documents and media library on your own NAS drive. But there’s one service that’s proven stubbornly tricky to replace — Google Photos. Out of all Google’s apps and services, Photos is the one that I use the most religiously. Whether it’s automatically backing up my phone’s photos, neatly organizing trips into albums, sharing snaps with family and friends, or quickly editing a pic when I’m not at my PC, Google Photos is a powerful one-stop-shop for everything mobile-photography related. As I’m sure you know.


Still, I’ve taken so many snaps over the years that I’ve hit Google Photos’ free 15GB limit. I’m reluctant to pay monthly for Google One storage when I have terabytes of disc space sitting idle on my home server. But breaking out from this particular Google service is harder than most.

***Google Photos alternatives for self-hosters***
**PhotoPrism gallery view**
There’s no shortage of self-hosted photo gallery applications out there, many of which are very powerful in their own right. Which is incredible, given they’re free too. Photoprism is a popular choice (and I’m currently using it), sporting machine learning capabilities to automatically tag and organize your photos. However, it currently lacks the multi-user capabilities a family needs and doesn’t have a first-party app to handle backups. LibrePhotos is another potent option, but I found the Android apps buggy (they’re still in early development) and couldn’t get it to play nicely with my library’s organizational structure.

There’s a great breakdown of Lychee, PiGallery, Piwigo, and others options to be found here, each of which comes with its own pros and cons. Ultimately, there’s a bit of a gap in the market for the seamless mobile backup and organizational experience Google offers. And that’s before we get into the fact that few of the options offer any editing capabilities whatsoever.

There's great gallery software aplenty, but few that provide an end-to-end photo backup solution.
All hope is not lost, though. The most Photos-like option currently out there is Immich. In fact, it’s designed to be a direct self-hosted competitor to Google Photos, right down to the interface style, support for multiple users, album sharing, and a bunch of other features.

**Immich — the best Google Photos alternative?**

At the time of writing, Immich is still in very active development and isn’t recommended as the only source for your photo backups just yet. Nevertheless, Immich already works really quite well as a self-hosted Google Photos alternative. Installation shouldn’t present any issues to those familiar with docker containers on their NAS.

Unlike most other options, there’s a working Android app for backups, complete with a gallery view. By design, it functions in much the same way as Google Photos, allowing you to select the folders you want to backup and displaying a little icon to indicate which photos are on-device and which are in your personal cloud. You can access your snaps through a web browser as well, which is where you’ll find all the server configuration options.

Immich also features basic machine learning for face recognition. It’s built on a rather primitive model, which is more hit-and-miss than Photos, but that should improve with time. There’s multi-user support, complete with album-sharing capabilities to mix snaps into family albums, the ability to share links externally, and reverse geocoding to flesh out the map interface.

Immich looks and feels very much like Google Photos, but you host it on your own PC.
If you know Photos, you’ll feel right at home with Immich. Despite missing more advanced Photos features like editing and highlight reels, it’s already almost solid enough to use as a daily driver. My only real complaint is that it doesn’t integrate into a complex existing library set up particularly well, with thumbnails stored next to the existing directories and new imports added to separate folders. Still, it’s an incredible piece of engineering for a passion project and could bloom into a viable Photos alternative after a few more months in development.

While I wait, I’ve settled for background syncing photos into organized folders using a separate backup app and viewing them via Photoprism at home. While on the go, it’s still impossible to beat the ease of use and features that Google Photos provides. I’ll just have to free up some space. With ongoing development, I’ll likely return to Immich in a few months and try to break free from Photos again.

**How to backup your Google Photos**

This whole experience also left me with some wisdom to impart regarding backing up your cloud snaps. If you’re eager to break away from Google Photos or just want a physical backup, the first step is to get your hands on your entire photo library via Google Takeout. While you can download snaps from Photos using various scripts, you’ll obtain the highest-quality file versions and complete metadata with Takeout.

Head into your account, untick everything except Google Photos, and pick the preferred size of your download zip files. I went with 10GB to avoid having a restart a huge download in the case of failure. Depending on the size of your library, it can take several hours for Google to send the email with your download links. Once you have it, proceed to download and unzip all your photos.

There are a few annoyances with Takeout’s photo organization, though. First, you’ll have to combine separate metadata JSON files back into your images for some ultra-irritating reason. Thankfully, there’s a handy application to fix this; simply point it to your extracted zip folder and wait. Secondly, there will be many duplicate photos, with Google providing images by both album and date. Worse, you’ll find varying file sizes in the different folders, making it difficult to track down the best duplicate to keep. I used Digikam to track down and remove the smaller duplicates, but this will require reorganizing some of your albums afterward.

**Managing automatic mobile photo backups**

While Immich is the most familiar way to backup your smartphone photos to a home server, other options exist. Scheduled backups directly to a shared SMB or WebDAV folder over your home Wi-Fi is one option, and several apps support this. PhotoSync is the most popular option, offering a gallery UI that allows you to see which photos have been backed up. It supports a wide range of backup services, including folder syncing, PhotoPrism, and cloud services like Photos and Box. It’s not free, but all the features can be had for less than $5. If you’re happy for everything to run in the background, Autosync or ZPush can handle backing up your camera folder but without a fancy UI to see what’s backed up.

While requiring setup on both ends, Resilio Sync or Syncthing offer robust file-syncing capabilities with additional capabilities over a basic network share, such as synching over the internet and across multiple computers and phones. Both have Android applications, but it’s worth remembering that neither is dedicated photo backup software, so don’t provide a Photos-esque experience.