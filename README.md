mundoplugs.com data
===================

The public domain data used to generate the [mundoplugs.com][1] Mains
Electricity Database.


Data
----

Data is in the [YAML][2] data serialization format.

  * `countries.yaml`
    * Primary key: ISO 3166-1 alpha-3 code (string, upper case)

  * `plugs.yaml`
    * Primary key: string, lower case, `[a-z0-9-]+`

  * `sockets.yaml`
    * Primary key: string, lower case, `[a-z0-9-]+`

Primary keys are unique among both `plugs.yaml` and `sockets.yaml`.


Photos
------

Photographs are TIFF format, 8-bit RGB, compressed with the LZW compression
scheme. The recommended dimensions are 1280x960 or 960x1280 pixels. An attempt
has been made to maintain relative scale between the images with 570 pixels
being approximately equivalent to 100mm. Files are named with the primary key
defined in the relevant YAML file with the extension "`.tif`" appended.

If submitting a pull request please ensure that photographic images comply with
these requirements.

Using [ImageMagick][3] to identify the compression scheme:

    $ identify -verbose image.tif | grep Compression

Using ImageMagick to compress a TIFF image:

    $ convert -compress lzw source.tif destination.tif


[1]: http://mundoplugs.com/
[2]: http://yaml.org/
[3]: http://www.imagemagick.org/

