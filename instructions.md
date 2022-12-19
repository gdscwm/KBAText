# KBA Scoping Portal instructions

The KBA Scoping Portal is currently in Beta release.  
There are a small number of known bugs; please follow the following instructions
to avoid them at this time.


## Suggested use

The tool can currently be used to scope:
* any number of drawn polygons
* a single uploaded file with one feature (polygon or multipolygon)

#### Drawing polygons

**Delete all shapes currently in the map tool before beginning a drawn session.**
This is a temporary measure to avoid a known bug.

Use the tools on the top-right of the map to draw and edit the areas you desire
to scope. Make sure that every drawn polygon has a unique name. It is only
possible to drawn simple shapes, i.e. with no lakes or islands. To scope more
comples geometries, draw them on a GIS software and upload them to be scoped.

Drawing an area that is too large is likely to result in very long
delays or the scope request to fail. Limitations over the maximum size of a
polygon are likely to be introduced in the future.

Once you have drawn an area you will be able to edit it by renaming it, moving
it, changing its vertices, and deleting it.

The online portal is currently stateless, meaning that if the webpage is closed
or refreshed, all progress is lost. For this reason, it is best that sites with
complex borders are first drawn on GIS software and then uploaded.


#### Uploading files

**Delete all shapes currently in the map tool before uploading a file.**
This is a temporary measure to avoid a known bug.

Make sure that the file coordinate reference system is EPSG:4326 (Decimal
Degrees & WGS84). The portal assumes this is the projection used, and uploading
a different one may raise an error or return a scoping of the wrong area.

Make sure the file you plan to upload contains no spaces in its filename.

Click on the **Upload data** button on the bottom-left and select a file. Most
GIS file formats are supported. ESRI _shp_ files should be compressed in a _zip_
file. Not supported: _kml_.

You will be asked to select a field to act as the feature name. Ensure that this
field does not contain repeated values.

Due to a current bug, only scope a single file with a single feature. 

#### Scoping and viewing results

Click on the **Query shapes** button on the bottom-right.

The legend shows the number of potential trigger species found at each site.
You can hover over each site to see all scoped parameters. You can change the
parameter displayed by the legend by selecting a different field in the bottom-left.

You can zoom to each scoped shape using the menu on the top-right.

#### Downloading results

You can either **Download All Data** or **Download Key Data**. The only
difference is that _all data_ will return _csv_ files with information on all
species found to intersect the polygon of interest, while _key data_ will only
return information on potential trigger species.

The downloaded file will also contain metadata files to help interpret the
contents of the downloaded scoping outputs.


## Bug reporting

Please report any issues you may find at the following link: [BUG REPORTING FORM](https://forms.gle/VZZPXoctt1qXpdJUA)
