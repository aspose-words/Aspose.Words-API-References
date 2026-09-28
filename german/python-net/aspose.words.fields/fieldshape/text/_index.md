---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fieldshape/text/
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
# Das BIDIOUTLINE-Feld nummeriert Absätze ähnlich wie die AUTONUM/LISTNUM-Felder,
# ist jedoch nur sichtbar, wenn eine Rechts-nach-Links-Bearbeitungssprache aktiviert ist, z. B. Hebräisch oder Arabisch.
# Das folgende Feld wird ".1" anzeigen, das RTL-Äquivalent der Listennummer "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Fügen Sie zwei weitere BIDIOUTLINE-Felder hinzu, die ".2" bzw. ".3" anzeigen.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Stellen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL ein.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Wenn wir in Microsoft Word eine Rechts-nach-Links-Bearbeitungssprache aktivieren, zeigen unsere Felder Zahlen an.
# Andernfalls zeigen sie "###" an.
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Öffnen Sie ein Dokument, das in Microsoft Word 2003 erstellt wurde.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Wenn wir das Word-Dokument öffnen und Alt+F9 drücken, sehen wir ein SHAPE- und ein EMBED-Feld.
# Ein SHAPE-Feld ist der Anker/Canvas für ein AutoShape-Objekt mit dem aktivierten Umbruchstil \"In line with text\".
# Ein EMBED-Feld hat dieselbe Funktion, jedoch für ein eingebettetes Objekt,
# wie zum Beispiel eine Tabelle aus einem externen Excel-Dokument.
# Allerdings werden diese Felder nicht in der Feldsammlung des Dokuments erscheinen.
self.assertEqual(0, doc.range.fields.count)
# Diese Felder werden nur von alten Versionen von Microsoft Word unterstützt.
# Der Ladevorgang des Dokuments wird diese Felder in Shape-Objekte konvertieren,
# auf die wir in der Knotensammlung des Dokuments zugreifen können.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# Der erste Shape-Knoten entspricht dem SHAPE-Feld im Eingabedokument,
# das das Inline-Canvas für die AutoShape ist.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# Der zweite Shape-Knoten ist die AutoShape selbst.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Der dritte Shape ist das frühere EMBED-Feld, das die externe Tabelle enthielt.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

