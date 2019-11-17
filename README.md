# ricemood
So you change your wallpaper? Of course you want the rice to match your wallpaper.

This tool is built for automate changing color manually. It basically templating engine for the color in configuration file.
## Quick Link > [Installation]() | [Example File]() 
You can set it to your :   
1. i3 config
2. terminal color scheme
3. svg icon file
4. The possibility are endless!

## Example File
> kitty terminal theme file
```javascript
kitty-theme.conf
...
background #$RM@DM>l(15)$
foreground #$RM@V>l(80)$

cursor #$RM@LightVibrant$

selection_background #$RM@Vibrant>lg(0.2)$
selection_foreground #$RM@V>ne$

color0 #$RM@DarkMuted>dk(0.1)$ 
color8 #$RM@DarkMuted>dk(0.2)$

color1 #$RM@Vibrant>l(60)$
color9 #$RM@Vibrant>l(70)$
...
```
>## Default Delimiter : [$RM, $]

## Function symbol
|symbol|description|example|
|-|-|-
|@|Choose color| @Vibrant
|>|Pipe color to various filter | @Vibrant>lighten(0.2)>sa(0.5)
|#|Choose color output|@Vibrant#rgb, @Vibrant#r 


## Color Name List
> Prefix : **@**
------------
|alias|full|example
|-|-|-
|V|Vibrant|
|LV|LightVibrant|
|DV|DarkVibrant
|M|Muted|
|LM|LightMuted|
|DM|DarkMuted|
|Q[0-20]|Color from quantize | @Q1 or @Quantizer1

## Pipe / Chaining
> Symbol : **>**

|alias|description|default parameter|
|-|-|-
|gr|grayscale|No parameter
|ne|negate|No parameter
|dk|darken|0.5
|lg|lighten|0.5
|de|desaturate|0.5
|sa|saturate|0.5
|wh|whiten|0.5
|bl|blacken|0.5
|fa|fade|0.5
|op|opaquer|0.5
|ro|rotate|90
|r|red|255
|g|green|255
|b|blue|255
|h|hue|255
|s|saturationl|255
|l|lightness|255

## Color Format
|format|example output|parameter|default|
|-|-|-|-
|hex   |FFFFFF (default) | None
|rgb   |255,255,255      | separator | ,  
|hsl   |255,255,255      | separator | ,
|r/g/b |255              | None
|h/s/l |255              | None