# Solar-X-Ray-Flare-Stats
This repository contains data and results files for analysis of Solar X-Ray flare rate statistic for cycles 21 to 25 in a text file format.

The data was originally obtained and reduced from the following locations:
X-ray flares prior to 1996: ftp://ftp.ngdc.noaa.gov/STP/space-weather/solar-data/solar-features/solar-flares/x-rays/goes/xrs/
X-ray flares from 1996 on can be found in the daily events lists at: ftp://ftp.swpc.noaa.gov/pub/warehouse/
Sunspot regions prior to 1996: ftp://ftp.ngdc.noaa.gov/STP/space-weather/solar-data/solar-features/sunspot-regions/usaf_mwl
Sunspot regions from 1996 on can be found in the daily sunspot region summary (SRS) files at: ftp://ftp.swpc.noaa.gov/pub/warehouse/

The file descriptions are given below.

flaretable.txt
Contains x-ray flares of M class or higher from 1986-03-23 to 2025-12-29.
One flare per line with the following format:
A2    Sunspot cycle number
A1    Blank
A19   Start time of the flare in the form %Y-%m-%dT%H:%M:%S
A1    Blank
A10   Peak time of the flare in the form %H:%M:%S
A1    Blank
A19   End time of the flare in the form %H:%M:%S
A1    Blank
I4    Four digit region identifier of the region the flare originated from. -1 indicates that the flares origin could not be identified
A1    Blank
A5    The x-ray class of the flare
A1    Blank
E7.1  The x-ray intensity in W/m^2
A1    Blank
A3    The McIntosh sunspot class of the flaring region. An entry of --- indicates the flare could not be matched to a region
A1    Blank
A3    The Mount Wilson Magnetic sunspot class of the flaring region. An entry of --- indicates the flare could not be matched to a region

regiontable.txt
Contains the number of regions for each McIntosh sunspot class for each cycle.
One McIntosh class per line with the following format:
A3    The McIntosh sunspot class
A1    Blank
I5    Number of regions for the McIntosh class in cycle 21
A1    Blank
I5    Number of regions for the McIntosh class in cycle 22
A1    Blank
I5    Number of regions for the McIntosh class in cycle 23
A1    Blank
I5    Number of regions for the McIntosh class in cycle 24
A1    Blank
I5    Number of regions for the McIntosh class in cycle 25

flareintensity.txt
Contains the table for the number of flares in given flare intensity categories in each cycle.
The first line is the header.
Each field is delimited by a pipe (|).
Field 1  Flare intensity category
Field 2  Number of flares for the intensity category in cycle 21
Field 3  Number of flares for the intensity category in cycle 22
Field 4  Number of flares for the intensity category in cycle 23
Field 5  Number of flares for the intensity category in cycle 24
Field 6  Number of flares for the intensity category in cycle 25

flarechi2.txt
Contains the table for the chi^2 test of the number of flares in each cycle.
The first line is the header.
Each field is delimited by a pipe (|).
Field 1  Cycles that are being compared
Field 2  Degrees of freedom
Field 3  Chi^2 test statistic
Field 4  p-value

flarerate_wilcoxon.txt
Contains the table for the Wilcoxon sign rank test of the flarerates by McIntosh class in each cycle.
The first line is the header.
Each field is delimited by a pipe (|).
Field 1  Cycles that are being compared
Field 2  Number of classes in the comparison
Field 3  Wilcoxon test statistic
Field 4  p-value

flarerate_wilcoxon.txt
Contains the table for the flare and region statistics for each sunspot cycle.
The first line contains the cycle numbers.
The second line is the header.
Each field is delimited by a pipe (|).
Field 1  McIntosh sunspot class
Field 2  Number of flares associated with the McIntosh class in cycle 21
Field 3  Number of region associated with the McIntosh class in cycle 21
Field 4  Flare rate per region associated with the McIntosh class in cycle 21
Field 5  Number of flares associated with the McIntosh class in cycle 22
Field 6  Number of region associated with the McIntosh class in cycle 22
Field 7  Flare rate per region associated with the McIntosh class in cycle 22
Field 8  Number of flares associated with the McIntosh class in cycle 23
Field 9  Number of region associated with the McIntosh class in cycle 23
Field 10  Flare rate per region associated with the McIntosh class in cycle 23
Field 11  Number of flares associated with the McIntosh class in cycle 24
Field 12  Number of region associated with the McIntosh class in cycle 24
Field 13  Flare rate per region associated with the McIntosh class in cycle 24
Field 14  Number of flares associated with the McIntosh class in cycle 25
Field 15  Number of region associated with the McIntosh class in cycle 25
Field 16  Flare rate per region associated with the McIntosh class in cycle 25

