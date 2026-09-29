---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /sv/python-net/aspose.words/paragraphformat/bidi/
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

Shows how to detect plaintext document text direction.

```python
# Skapa ett "TxtLoadOptions"‑objekt, som vi kan skicka till ett dokuments konstruktor
# för att ändra hur vi laddar ett klartext‑dokument.
load_options = aw.loading.TxtLoadOptions()
# Ställ in egenskapen "DocumentDirection" till "DocumentDirection.Auto" som automatiskt upptäcker
# riktningen för varje textparagraf som Aspose.Words laddar från klartext.
# Varje paragrafens "Bidi"‑egenskap kommer att lagra dess riktning.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Detektera hebreisk text som höger‑till‑vänster.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Detektera engelsk text som höger‑till‑vänster.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

