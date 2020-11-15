# How to reduce image size and then create an A4 pdf

## STEP1 : How to convert list of images only density and quality.

This will reduce the file size significantly

```
for f in *.png;  do
convert ${f} -quality 40% -strip -density 1000x1000 ${f}.mod.jpg 
done;
```

## STEP2: how to create a A4 pdf from set of images

$ convert *.jpg -density 80.9428 -units pixelspercentimeter -resize 1700x2404 -background white -gravity center -extent 1700x2404 multi2.pdf



# HOW TO CONVERT AN IMAGE TO DESIRED 
DPI (1000x1000) AND   
SIZE (2000x1044) AND   
QUALITY (40%) AND   
SHARPEN (0x0.55+0.55+0.008)  

```
convert IMG_20200704_112557_result.jpg -unsharp 0x0.55+0.55+0.008 -quality 40% -strip -density 1000x1000 -resize 2000x1044 -background white -gravity center -extent 2000x1044 result_IMG_20200704_112557.jpg
```

