```
library(plotGoogleMaps)
library(RColorBrewer)
vignette('plotGoogleMaps-intro')

coordinates(data) <- ~artist.longitude
+ artist.latitude
coordinates(data) <- ~artist.longitude
+ artist.latitude

proj4string(data) <-
+ CRS("+init=epsg:4326")

m <- bubbleGoogleMaps(data,
zcol='sa.hf', filename = 'map.html',
mapTypeId= 'TERRAIN', fitBounds=T,
max.radius=75000,
key.entries= c( 1.05,1.1,1.25,max),
colPalette=brewer.pal(4,"YlOrRd"),
layerName="Ratio of Song Hotness to
Artist Familiarity")

```
