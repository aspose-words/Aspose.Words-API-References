---
title: ImageData.gray_scale property
linktitle: gray_scale property
articleTitle: gray_scale property
second_title: Aspose.Words for Python
description: "ImageData.gray_scale property. Determines whether a picture will display in grayscale mode."
type: docs
weight: 100
url: /sv/python-net/aspose.words.drawing/imagedata/gray_scale/
---

## ImageData.gray_scale property

Determines whether a picture will display in grayscale mode.


```python
@property
def gray_scale(self) -> bool:
    ...

@gray_scale.setter
def gray_scale(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# Importera en form från källdokumentet och lägg till den i det första stycket.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# Den importerade formen innehåller en bild. Vi kan komma åt bildens egenskaper och rådata via ImageData-objektet.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Om en bild saknar kanter kommer dess ImageData-objekt att definiera kantfärgen som tom.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Den här bilden länkar inte till en annan form eller bildfil i det lokala filsystemet.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# Egenskaperna \"Brightness\" och \"Contrast\" definierar bildens ljusstyrka och kontrast
# på en skala från 0 till 1, med standardvärdet på 0.5.
image_data.brightness = 0.8
image_data.contrast = 1
# Ovanstående ljusstyrke- och kontrastvärden har skapat en bild med mycket vitt.
# Vi kan välja en färg med egenskapen ChromaKey för att ersätta med transparens, till exempel vitt.
image_data.chroma_key = aspose.pydrawing.Color.white
# Importera källformen igen och ställ in bilden på monokrom.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Importera källformen igen för att skapa en tredje bild och ställ in den på BiLevel.
# BiLevel sätter varje pixel till antingen svart eller vitt, beroende på vilket som är närmare den ursprungliga färgen.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# Beskärning bestäms på en skala från 0 till 1. Beskär en sida med 0,3
# kommer att beskära 30% av bilden på den beskurna sidan.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

