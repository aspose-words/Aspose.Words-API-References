---
title: ImageData.gray_scale property
linktitle: gray_scale property
articleTitle: gray_scale property
second_title: Aspose.Words for Python
description: "ImageData.gray_scale property. Determines whether a picture will display in grayscale mode."
type: docs
weight: 100
url: /it/python-net/aspose.words.drawing/imagedata/gray_scale/
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
# Importa una forma dal documento sorgente e aggiungila al primo paragrafo.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# La forma importata contiene un'immagine. Possiamo accedere alle proprietà dell'immagine e ai dati grezzi tramite l'oggetto ImageData.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Se un'immagine non ha bordi, il suo oggetto ImageData definirà il colore del bordo come vuoto.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Questa immagine non è collegata a un'altra forma o file immagine nel file system locale.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# Le proprietà "Brightness" e "Contrast" definiscono la luminosità e il contrasto dell'immagine
# su una scala da 0 a 1, con il valore predefinito a 0,5.
image_data.brightness = 0.8
image_data.contrast = 1
# I valori di luminosità e contrasto sopra indicati hanno creato un'immagine con molto bianco.
# Possiamo selezionare un colore con la proprietà ChromaKey da sostituire con trasparenza, ad esempio il bianco.
image_data.chroma_key = aspose.pydrawing.Color.white
# Importa nuovamente la forma di origine e imposta l'immagine in monocromo.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Importa nuovamente la forma di origine per creare una terza immagine e impostala su BiLevel.
# BiLevel imposta ogni pixel su nero o bianco, a seconda di quale sia più vicino al colore originale.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# Il ritaglio è determinato su una scala da 0 a 1. Ritagliare un lato di 0,3
# ritaglierà il 30% dell'immagine sul lato ritagliato.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

