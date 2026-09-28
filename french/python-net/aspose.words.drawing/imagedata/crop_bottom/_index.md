---
title: ImageData.crop_bottom property
linktitle: crop_bottom property
articleTitle: crop_bottom property
second_title: Aspose.Words for Python
description: "ImageData.crop_bottom property. Defines the fraction of picture removal from the bottom side."
type: docs
weight: 60
url: /fr/python-net/aspose.words.drawing/imagedata/crop_bottom/
---

## ImageData.crop_bottom property

Defines the fraction of picture removal from the bottom side.


```python
@property
def crop_bottom(self) -> float:
    ...

@crop_bottom.setter
def crop_bottom(self, value: float):
    ...

```

### Remarks

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note 
that a value of 1 will display no picture at all. Negative values will result in 
the picture being squeezed inward from the edge being cropped (the empty space 
between the picture and the cropped edge will be filled by the fill color of the 
shape). Positive values less than 1 will result in the remaining picture being 
stretched to fit the shape.

The default value is 0.




### Examples

Shows how to edit a shape's image data.

```python
img_source_doc = aw.Document(file_name=MY_DIR + 'Images.docx')
source_shape = img_source_doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
dst_doc = aw.Document()
# Importez une forme du document source et ajoutez‑la au premier paragraphe.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
# La forme importée contient une image. Nous pouvons accéder aux propriétés de l'image et aux données brutes via l'objet ImageData.
image_data = imported_shape.image_data
image_data.title = 'Imported Image'
self.assertTrue(image_data.has_image)
# Si une image n'a pas de bordures, son objet ImageData définira la couleur de bordure comme vide.
self.assertEqual(4, image_data.borders.count)
self.assertEqual(aspose.pydrawing.Color.empty(), image_data.borders[0].color)
# Cette image ne lie pas à une autre forme ou fichier image dans le système de fichiers local.
self.assertFalse(image_data.is_link)
self.assertFalse(image_data.is_link_only)
# Les propriétés "Brightness" et "Contrast" définissent la luminosité et le contraste de l'image
# sur une échelle de 0 à 1, avec la valeur par défaut à 0,5.
image_data.brightness = 0.8
image_data.contrast = 1
# Les valeurs de luminosité et de contraste ci-dessus ont créé une image très blanche.
# Nous pouvons sélectionner une couleur avec la propriété ChromaKey pour la remplacer par de la transparence, comme le blanc.
image_data.chroma_key = aspose.pydrawing.Color.white
# Importez à nouveau la forme source et définissez l'image en monochrome.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.gray_scale = True
# Importez à nouveau la forme source pour créer une troisième image et définissez-la en BiLevel.
# BiLevel définit chaque pixel en noir ou blanc, selon ce qui est le plus proche de la couleur originale.
imported_shape = dst_doc.import_node(src_node=source_shape, is_import_children=True).as_shape()
dst_doc.first_section.body.first_paragraph.append_child(imported_shape)
imported_shape.image_data.bi_level = True
# Le recadrage est déterminé sur une échelle de 0 à 1. Recadrer un côté de 0,3
# coupera 30 % de l'image du côté recadré.
imported_shape.image_data.crop_bottom = 0.3
imported_shape.image_data.crop_left = 0.3
imported_shape.image_data.crop_top = 0.3
imported_shape.image_data.crop_right = 0.3
dst_doc.save(file_name=ARTIFACTS_DIR + 'Drawing.ImageData.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ImageData](../)

