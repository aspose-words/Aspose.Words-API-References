---
title: Watermark.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for Python
description: "Watermark.type property. Gets the watermark type."
type: docs
weight: 10
url: /fr/python-net/aspose.words/watermark/type/
---

## Watermark.type property

Gets the watermark type.


```python
@property
def type(self) -> aspose.words.WatermarkType:
    ...

```

### Examples

Shows how to create a text watermark.

```python
doc = aw.Document()
# Ajoutez un filigrane en texte brut.
doc.watermark.set_text(text='Aspose Watermark')
# Si nous souhaitons modifier le formatage du texte en l'utilisant comme filigrane,
# nous pouvons le faire en passant un objet TextWatermarkOptions lors de la création du filigrane.
text_watermark_options = aw.TextWatermarkOptions()
text_watermark_options.font_family = 'Arial'
text_watermark_options.font_size = 36
text_watermark_options.color = aspose.pydrawing.Color.black
text_watermark_options.layout = aw.WatermarkLayout.DIAGONAL
text_watermark_options.is_semitrasparent = False
doc.watermark.set_text(text='Aspose Watermark', options=text_watermark_options)
doc.save(file_name=ARTIFACTS_DIR + 'Document.TextWatermark.docx')
# Nous pouvons supprimer un filigrane d'un document de cette façon.
if doc.watermark.type == aw.WatermarkType.TEXT:
    doc.watermark.remove()
```

### See Also

* module [aspose.words](../../)
* class [Watermark](../)

