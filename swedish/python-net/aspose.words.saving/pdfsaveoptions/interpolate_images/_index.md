---
title: PdfSaveOptions.interpolate_images property
linktitle: interpolate_images property
articleTitle: interpolate_images property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.interpolate_images property. A flag indicating whether image interpolation shall be performed by a conforming reader"
type: docs
weight: 230
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/interpolate_images/
---

## PdfSaveOptions.interpolate_images property

A flag indicating whether image interpolation shall be performed by a conforming reader.
When ``False`` is specified, the flag is not written to the output document and
the default behaviour of reader is used instead.



```python
@property
def interpolate_images(self) -> bool:
    ...

@interpolate_images.setter
def interpolate_images(self, value: bool):
    ...

```

### Remarks

When the resolution of a source image is significantly lower than that of the output device,
each source sample covers many device pixels. As a result, images can appear jaggy or blocky.
These visual artifacts can be reduced by applying an image interpolation algorithm during rendering.
Instead of painting all pixels covered by a source sample with the same color, image interpolation
attempts to produce a smooth transition between adjacent sample values.

A conforming Reader may choose to not implement this feature of PDF,
or may use any specific implementation of interpolation that it wishes.

The default value is ``False``.

Interpolation flag is prohibited by PDF/A compliance. ``False`` value will be used automatically
when saving to PDF/A.




### Examples

Shows how to perform interpolation on images while saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
save_options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "InterpolateImages" till "true" för att få läsaren som öppnar detta dokument att interpolera bilder.
# Deras upplösning bör vara lägre än den på enheten som visar dokumentet.
# Ställ in egenskapen "InterpolateImages" till "false" för att göra så att läsaren inte tillämpar någon interpolering.
save_options.interpolate_images = interpolate_images
# När vi öppnar detta dokument med en läsare som Adobe Acrobat, måste vi zooma in på bilden
# för att se interpoleringseffekten om vi sparade dokumentet med den aktiverad.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.InterpolateImages.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

