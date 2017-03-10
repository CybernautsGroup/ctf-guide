## Bypassing redacted PDF:s





http://forensicswiki.org/wiki/PDF

### Simple copy-paste technique

If the text is still interpreted as text, and not as an image, you can simply just copy and paste the text even though it might contain black boxes above the text. This is illustrated in this video:

https://vimeo.com/1451028

Here is a practical example to test it on: http://static.cbslocal.com/station/wbbm/obama.pdf



### Pdfimages - separating images

The PDF format supports embedding other files inside the PDF. So if you have a PDF that has black boxes over certain words it might just be separated images in the file. So we can separate those images with the help of `pdfimages`.

```
pdfimages File.pdf  outfile  
```



