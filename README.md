# EXTRACT-COLOUR-FROM-IMAGE
Python based REST API to extract important color from an image.

pip install colorgram.py
pip install colorthief

import colorgram
colors = colorgram.extract('https://storage.googleapis.com/bizupimg/profile_photo/WhatsApp%20Image%202020-08-23%20at%203.11.46%20PM%20-%20Himanshu%20Kohli.jpeg', 6)

# color of image border

first_color = colors[0]
rgb = first_color.rgb 
hsl = first_color.hsl 
proportion  = first_color.proportion
red = rgb[0]
red = rgb.r
saturation = hsl[1]
saturation = hsl.s


from colorthief import ColorThief
color_thief = ColorThief('https://storage.googleapis.com/bizupimg/profile_photo/WhatsApp%20Image%202020-08-23%20at%203.11.46%20PM%20-%20Himanshu%20Kohli.jpeg')
# get the dominant color
dominant_color = color_thief.get_color(quality=1)

