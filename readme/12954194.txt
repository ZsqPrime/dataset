daily-quote-bash
================
 
Labels
notify-send, Linux, wget, sed, compliments, JAMESJARA

Script bash para generar frases de piropos aleatorios en bash
Muestra un popup con el contenido unico de un piropo aleatorio.

Bash script to generate random phrases bash compliments
Shows a popup with the contents of a single random compliment.

```bash
#!/bin/sh

#url
url='http://gadget.citasyrefranes.com/gadget_xml.php?t=PI&r=83'

#get data
data=` wget -q -O - $url | sed -n -e 's/.*<texto>\(.*\)<\/texto>.*/\1/p'`

#create notification
notify-send "Frase Piropo" "${data}"

```
