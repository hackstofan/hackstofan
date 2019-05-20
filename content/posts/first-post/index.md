---
title: "Hvernig þú getur skrifað greinar fyrir Hackstofuna."
date: 2019-03-10T04:05:57Z
author: "Hermann Björgvin"
draft: true
featured_image: images/developers.jpg
tags:
- Development
- Go
---

##### Viltu verða penni?
Það er ekki svo flókið. Með því að lesa þessa grein verður þú fljótt fær í því að smíða hágæða greinar sem snúa að vinnu þinni. Aðdáendur verða margir, samstarfsmenn þakklátir, en ekki láta frægðina stíga þér til höfuðs því það er **alltaf** fleira sem við getum lært.

Uppsetning er ekki flóknari en að keyra eftirfarandi skipanir í skel þinni, windows eða linux terminal.

`git clone git@github.com:hackstofan/hackstofan.git`

`cd hackstofan`

`sudo docker-compose up`

##### Sýndu smá lit! Hvernig vilt þú tjá þig?
Lof mér að kynna fyrir þér þeim tólum sem þú hefur til taks þegar þú skrifar þína grein. Oft finnur maður löngun til þess að vísa til fyrri áhrifavalda. Hér er dæmi um slíka flotta og stóra tilvísun. Sem hægt er að skoða í skránni á bakvið þessa grein.

> <h6>"Truth can only be found in one place: the code."</h6><br>
> -- Robert C. Martin

##### Guð blessi þá sem skrifa kóða!
Þegar þú skrifar kóða þá viltu að hann sé læsilegur, en hvernig gerir maður það á vefnum? Hér fyrir neðan má sjá dæmi um Mandelbrot mengið reiknað í R. Þú getur skoðað hvernig ég fer að þessu með því að líta á þessar [leiðbeiningar](https://gohugo.io/content-management/syntax-highlighting/).

{{< highlight r "linenos=table,style=friendly" >}}
library(ggplot2)
 
mb <- mandelbrot(xlim = c(-0.8335, -0.8325),
                 ylim = c(0.205, 0.206),
                 resolution = 1200L,
                 iterations = 1000)
 
# vaccination heatmap palette
cols <- c(
  colorRampPalette(c("#e7f0fa", "#c9e2f6", "#95cbee",
                     "#0099dc", "#4ab04a", "#ffd73e"))(10),
  colorRampPalette(c("#eec73a", "#e29421", "#e29421",
                     "#f05336","#ce472e"), bias=2)(90),
  "black")
 
df <- as.data.frame(mb)
ggplot(df, aes(x = x, y = y, fill = value)) +
  geom_raster(interpolate = TRUE) + theme_void() +
  scale_fill_gradientn(colours = cols, guide = "none")
{{< / highlight >}}