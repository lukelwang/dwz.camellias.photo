# DWZ Camellia Photos

Public photo and album storage for [花间](https://lukelwang.github.io/dwz.camellias/). Managed by the single owner, `lukelwang`, through the gallery.

- `gallery.json` is the public album/settings index (schema version 1).
- `photos/<photo-id>/image.jpg` is a display JPEG, longest edge up to 2560 pixels.
- `photos/<photo-id>/thumbnail.jpg` is the gallery thumbnail, longest edge up to 640 pixels.
- Capture time and its EXIF/manual source are stored in the index; embedded EXIF is removed from generated JPEGs. Original files remain in the owner's photo library and are not archived here.
- A batch writes its images, thumbnails and index in one Git commit. Concurrent edits are rejected rather than overwritten.
- Deletions remove files from the current branch; earlier commits retain recovery history.

No credentials belong in this repository. The web page keeps the owner's GitHub token only in current-page memory and sends it only to the GitHub API. Visitors read public data without a token.

The repository starts empty; prototype reference images are not copied here.
