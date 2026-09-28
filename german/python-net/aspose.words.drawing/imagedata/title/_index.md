---
title: ImageData.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "ImageData.title property. Defines the title of an image."
type: docs
weight: 180
url: /de/python-net/aspose.words.drawing/imagedata/title/
---

## ImageData.title property

Defines the title of an image.


```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Remarks

The default value is an empty string.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# Importieren Sie eine Form aus dem Quelldokument und fügen Sie sie dem ersten Absatz hinzu.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# Die importierte Form enthält ein Bild. Wir können über das ImageData-Objekt auf die Eigenschaften und Rohdaten des Bildes zugreifen.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Wenn ein Bild keine Ränder hat, definiert sein ImageData-Objekt die Randfarbe als leer.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Dieses Bild verlinkt nicht zu einer anderen Form oder Bilddatei im lokalen Dateisystem.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# Die "Brightness"- und "Contrast"-Eigenschaften definieren die Helligkeit und den Kontrast des Bildes
# auf einer Skala von 0-1, wobei der Standardwert bei 0,5 liegt.
image_data.brightness = 0.8
image_data.contrast = 1
# Die obigen Helligkeits- und Kontrastwerte haben ein Bild mit viel Weiß erzeugt.
# Wir können eine Farbe mit der ChromaKey-Eigenschaft auswählen, um sie durch Transparenz zu ersetzen, zum Beispiel Weiß.
image_data.chroma_key = aspose.pydrawing.Color.white
# Importieren Sie die Quellform erneut und setzen Sie das Bild auf Monochrom.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Importieren Sie die Quellform erneut, um ein drittes Bild zu erstellen, und setzen Sie es auf BiLevel.
# BiLevel setzt jedes Pixel entweder auf Schwarz oder Weiß, je nachdem, welche Farbe dem Originalfarbwert näher liegt.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# Das Zuschneiden wird auf einer Skala von 0-1 bestimmt. Eine Seite um 0,3 zuschneiden
# schneidet 30 % des Bildes an der beschnittenen Seite ab.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

