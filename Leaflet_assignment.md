R Markdown
----------

popdata\_india &lt;- read.csv(“India\_population\_lat\_long.csv”)
colnames(popdata\_india) &lt;- c(“State”, “latitude”,
“longitude”,“population”)

popdata\_india*p**o**p**s**e**p* &lt;  − *f**o**r**m**a**t*(*p**o**p**d**a**t**a*<sub>*i*</sub>*n**d**i**a*population,big.mark=“,”,scientific=FALSE)
popdata\_india$pop &lt;- do.call(paste, c(popdata\_india\[c(“State”,
“popsep”)\], sep = " population:"))

library(leaflet) options(viewer = NULL) india\_pop\_map &lt;-
popdata\_india %&gt;% leaflet() %&gt;% addTiles() %&gt;%
addCircles(weight = 1, radius =
(popdata\_india*p**o**p**u**l**a**t**i**o**n*)/1000, *p**o**p**u**p* = *s**t**r**w**r**a**p*(*p**o**p**d**a**t**a*<sub>*i*</sub>*n**d**i**a*pop))

india\_pop\_map

library(htmlwidgets) saveWidget(india\_pop\_map,
file=“india\_pop\_map.html”,title = “19-May-2019”)
