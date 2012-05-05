# About

OGR based Python tools for querrying a data source (SHP, etc) and drawing thematic cartographic representations.

By Nathaniel Vaughn Kelso at Stamen.

Stubs out MSS and MML files based on a dataset for:

* Quick data exploration of what's in a dataset
* Refined cartographic presentations


## Installation

Git checkout (requires git)

    git clone git://github.com/nvkelso/thematic-carto-tools.git
    cd thematic-carto-tools
    
Includes built in support for CSV/TSV and DBF/SHP files. Uses OGR for other file types.


## Usage

Just a single sympol:

    python thematic.py --in_file=sample_data/ne_10m_admin_0_countries.shp

Classify a polygon/polyline dataset in 5 steps (default is: --legend-type=quantile -n 5):

    python thematic.py --in_file=sample_data/ne_10m_admin_0_countries.shp --indicator=POP_EST

Separate color for each feature value:

    python thematic.py --in_file=sample_data/ne_10m_admin_0_countries.shp --indicator=MAP_COLOR --classification-type=unique-value

Will create 3 files:

1. `style.mml` - Cascadenik map markup layer file
2. `stylesheet.mss` - Cascadenik map style sheet file
3. `legend.html` - See the color breaks in a pretty HTML legend

These files are writen local to where you ran the script. Use the "--out_files" option to specify different names.
    

## Requirements

- Python `>= 2.6`

- GDAL with OGR support `>= ?`


## Author

- Nathaniel V. KELSO (nvkelso)

### Contributors

- Michael Lawrence Evans (mlevans)
- Mike Migurski (migurski)


## Coda

Inspired by a fall 2011 workshop held at Stamen about future of Carto and Cascadenik CSS style map rendering in Mapnik & etc.