# timelapse-compression

## A git repository created by Andrew Schmidt (andrewschmidt.xyz)

### An idea in the pre-development phase

The idea behind this repo: Compress hundreds of photos into an archive of
smaller or equal storage size to save room on my computer.

This will exploit the fact that local images in a timelapse do not have many differences ,
despite the fact that the video does change in the long run.

## The General Idea

* Take hundreds of photos in a file folder on the computer.
These photos should be a timelapse sequence of TIFFs.

* The compression will take these photos and merge them into an archive to save space

* The idea is that you can store the first image and for the next x images store
the pixel-by-pixel difference of that image and the first.
This storage method should take up less space than the original storage method

* Keep storing differences until the difference is sufficiently large
When this happens acquire a new reference image and repeat.

* The archive file format (.TLI (timelapse image archive) will not display
previews of the files. It will act like a .zip and must be decompressed to
view/edit the photos
