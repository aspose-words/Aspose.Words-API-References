---
title: ImageSaveOptions.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for Python
description: "ImageSaveOptions.clone method. Creates a deep clone of this object."
type: docs
weight: 200
url: /de/python-net/aspose.words.saving/imagesaveoptions/clone/
---

## clone() {#default}

Creates a deep clone of this object.


```python
def clone(self):
    ...
```

### Examples

Shows how to select a bit-per-pixel rate with which to render a document to an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions-Objekt übergeben, um
# ein Pixel-Format für das Bild auszuwählen, das der Speichervorgang erzeugt.
# Verschiedene Bits‑pro‑Pixel‑Raten beeinflussen die Qualität und Dateigröße des erzeugten Bildes.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.pixel_format = image_pixel_format
# Wir können ImageSaveOptions-Instanzen klonen.
self.assertNotEqual(image_save_options, image_save_options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.PixelFormat.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

