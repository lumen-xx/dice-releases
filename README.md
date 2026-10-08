# Dice

A small native Mac app to convert, resize and compress images, inspect metadata and remove personal tags. Everything happens locally on your Mac. Originals stay untouched.

[Download the latest preview](https://github.com/lumen-xx/dice-releases/releases/latest)

![Dice image editor](images/image.png)

- Convert to JPEG, PNG, HEIC or WebP.
- Resize by longest edge, percentage or a bounding box.
- Compress lossy images with a quality slider; export lossless WebP.
- Remove personal metadata, including a metadata-only mode that keeps pixels unchanged.
- Browse complete textual ExifTool metadata, search/filter tags and copy individual values or export JSON.
- Search batches by filename, metadata, dimensions or recognized image text.

![Dice metadata viewer](images/metadata.png)

## Getting started

Requires **macOS 14 or newer and an Apple-silicon Mac**. The app is about **26.2 MB installed / 7.8 MB downloaded**. ExifTool and WebP tools are bundled.

1. Download the ZIP from [Releases](https://github.com/lumen-xx/dice-releases/releases/latest).
2. Unzip it and move **Dice.app** into **Applications**.
3. Open Dice and drop images into its window, use **+**, or choose **Open With → Dice** in Finder.
4. Choose your conversion settings and press **Start**. Use the down-arrow to save processed copies.

The page number opens the searchable image list. Removing an image from Dice leaves its original file in place. Save your processed copies before closing the app.

![Dice image list](images/batch.png)

## First launch: macOS approval

This preview is not yet Developer ID signed or notarized. macOS may block the first downloaded copy. Only follow these steps for Dice downloaded from this repository.

### System Settings

1. Try opening Dice once.
2. Open **System Settings → Privacy & Security**.
3. Scroll to the Dice security message and click **Open Anyway**.
4. Confirm **Open** and authenticate if asked.

[Apple’s instructions](https://support.apple.com/en-us/102445) explain the same process.

### Terminal

With Dice in Applications, paste this into Terminal:

```sh
xattr -dr com.apple.quarantine /Applications/Dice.app
```

Then open Dice. This removes the download quarantine flag from **Dice only**, without disabling Gatekeeper for other apps. Use the correct app path if you installed it elsewhere.

## Updates

Use **Dice → Check for Updates…** to get later versions directly from GitHub. Updates and the update feed are signed. Preview releases are enabled by default; turn off **Include Preview Releases** to follow stable releases only. Checks are manual, and no GitHub account is required.

Use the in-app updater after the first approval. Downloading another ZIP through a browser can trigger macOS approval again. Update signatures do not replace Apple notarization.

## Preview limits

PNG re-encoding can increase file size. Conversion rejects animated/multi-image files rather than discard frames. JPEG flattens transparency onto white; HDR conversion is not preserved as HDR. Metadata removal does not anonymize filenames or file-system attributes. Intel builds and clean-machine compatibility testing are still pending.

This repository contains compiled downloads, screenshots, release notes and the signed update feed. The Dice source repository is private.
