# Dice

## Install

macOS 14+ · Apple silicon

1. [Download Dice](https://github.com/lumen-xx/dice-releases/releases), unzip and move **Dice.app** to **Applications**.
2. Open Dice. If blocked, go to **System Settings → Privacy & Security → Open Anyway**, or run:

```sh
xattr -dr com.apple.quarantine /Applications/Dice.app
```

Use this only for Dice downloaded here. This preview is not yet notarized.

A small native Mac app to convert, resize and compress images, inspect metadata and remove personal tags. Everything happens locally on your Mac. Originals stay untouched.

![Dice image editor](images/image.png)

- Convert to JPEG, PNG, HEIC or WebP.
- Resize by longest edge, percentage or a bounding box.
- Compress lossy images with a quality slider; export lossless WebP.
- Remove personal metadata, including a metadata-only mode that keeps pixels unchanged.
- Browse complete textual ExifTool metadata, search/filter tags and copy individual values or export JSON.
- Search batches by filename, metadata, dimensions or recognized image text.

![Dice metadata viewer](images/metadata.png)

## Using Dice

Requires **macOS 14 or newer and an Apple-silicon Mac**. The app is about **26.2 MB installed / 7.8 MB downloaded**. ExifTool and WebP tools are bundled.

Drop images into Dice, use **+**, or choose **Open With → Dice** in Finder. Choose your settings and press **Start**; the down-arrow saves processed copies.

The page number opens the searchable image list. Removing an image from Dice leaves its original file in place. Save your processed copies before closing the app.

![Dice image list](images/batch.png)

## Updates

Use **Dice → Check for Updates…** to get later versions directly from GitHub. Updates and the update feed are signed. Preview releases are enabled by default; turn off **Include Preview Releases** to follow stable releases only. Checks are manual, and no GitHub account is required.

Use the in-app updater after the first approval. Downloading another ZIP through a browser can trigger macOS approval again. Update signatures do not replace Apple notarization.

## Preview limits

PNG re-encoding can increase file size. Conversion rejects animated/multi-image files rather than discard frames. JPEG flattens transparency onto white; HDR conversion is not preserved as HDR. Metadata removal does not anonymize filenames or file-system attributes. Intel builds and clean-machine compatibility testing are still pending.

This repository contains compiled downloads, screenshots, release notes and the signed update feed. The Dice source repository is private.
