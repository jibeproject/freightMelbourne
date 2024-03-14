# freightMelbourne
This repository contains code for the Melbourne freight model.

# Overview
There is one script file, `freight.R`, which allocates freight volumes to network links.

It can be used in two versions:
- matsim output - produces origin and destination addresses for trips, used as an input for matsim to run the routing.
- full output - also runs the routing and calculates freight volumes for each link.

The matsim output is the version used in the JIBE model.

# Input files
The code requires the following input files, which are available [to authorised users] at [*insert location when known*].  The code assumes that the input files are located in a `data` directory ("../data/") which sits beside the directory in which the script files are located .

| File               | Content                                                  |
|--------------------|----------------------------------------------------------|
|*data/original/DTP freight* |Folder containing matrices of vehicle demand by time period and associated spatial data |
|*data/original/1270055001_mb_2016_vic_shape.zip* |ABS 2016 census meshblocks for Victoria|
|*data/original/VIC_ADDRESS_DEFAULT_GEOCODE_psv.psv* |Geocoded National Address File (GNAF) points for Victoria |
|*data/processed/edgesMelbourne.gpkg* & *data/processed/nodesMelbourne.gpkg* |Edges and nodes making up the road network |

# Output files
The code produces the following output files, which are saved to the `data\processed` directory.

| File               | Content                                                  |
|--------------------|----------------------------------------------------------|
|*freight_trips_with_ODs.csv* | Matsim output: origin and destination addresses for freight trips |
|*freight_volumes.csv* | Full output: network links with freight volumes by link |
