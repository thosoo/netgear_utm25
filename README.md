# Netgear UTM25
Findings about the Netgear UTM25

Hardware details about this device can be found here:
https://deviwiki.com/wiki/Netgear_ProSecure_UTM25

To get into U-Boot use the U-Boot command with the following password:
```
enable_admin N2T8G7R5U3T6M9
```
This is true for UTM5, UTM10 and UTM25.

UTM25 has the same board rev number as `UBIQUITI_E120` which is `20004`, but has only a single core.
However, stock uboot differentiates the board as following:
```
gd->board_desc.board_type = CVMX_BOARD_TYPE_CUST_UTM25; // Board type definition from toolchain executive and it will be passed to kernel	
gd->board_desc.rev_major = 2;
```
