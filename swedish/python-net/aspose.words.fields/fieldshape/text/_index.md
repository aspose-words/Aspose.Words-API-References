---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# BIDIOUTLINE-fältet numrerar stycken som AUTONUM/LISTNUM-fälten,
# men är endast synligt när ett höger-till-vänster redigeringsspråk är aktiverat, såsom hebreiska eller arabiska.
# Följande fält kommer att visa ".1", den RTL-ekvivalenten till listnumret "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Lägg till två ytterligare BIDIOUTLINE-fält, som kommer att visa ".2" och ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Ställ in horisontell textjustering för varje stycke i dokumentet till RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Om vi aktiverar ett höger-till-vänster redigeringsspråk i Microsoft Word kommer våra fält att visa siffror.
# Annars kommer de att visa "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Öppna ett dokument som skapades i Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Om vi öppnar Word-dokumentet och trycker på Alt+F9, kommer vi att se ett SHAPE- och ett EMBED-fält.
# Ett SHAPE-fält är ankaret/ytan för ett AutoShape-objekt med omslagstilen "In line with text" aktiverad.
# Ett EMBED-fält har samma funktion, men för ett inbäddat objekt,
# till exempel ett kalkylblad från ett externt Excel-dokument.
# Dessa fält kommer dock inte att visas i dokumentets Fields-samling.
self.assertEqual(0, doc.range.fields.count)
# Dessa fält stöds endast av äldre versioner av Microsoft Word.
# Dokumentläsningsprocessen kommer att konvertera dessa fält till Shape-objekt,
# som vi kan komma åt i dokumentets node-samling.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# Den första Shape-noden motsvarar SHAPE-fältet i indatadokumentet,
# som är den inbäddade ytan för AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# Den andra Shape-noden är själva AutoShape.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Den tredje Shape är det som var EMBED-fältet som innehöll det externa kalkylbladet.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

