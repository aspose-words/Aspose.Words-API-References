---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /de/python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




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

Shows how to detect plaintext document text direction.

```python
# Erstellen Sie ein "TxtLoadOptions"‑Objekt, das wir an den Konstruktor eines Dokuments übergeben können
# um zu ändern, wie wir ein Klartextdokument laden.
load_options = aw.loading.TxtLoadOptions()
# Setzen Sie die Eigenschaft "DocumentDirection" auf "DocumentDirection.Auto", erkennt automatisch
# die Richtung jedes Textabsatzes, den Aspose.Words aus Klartext lädt.
# Die "Bidi"‑Eigenschaft jedes Absatzes speichert dessen Richtung.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Hebräischen Text als Rechts‑nach‑Links erkennen.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Englischen Text als Rechts‑nach‑Links erkennen.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

