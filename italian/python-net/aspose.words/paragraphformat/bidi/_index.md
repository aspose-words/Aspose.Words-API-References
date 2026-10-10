---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /it/python-net/aspose.words/paragraphformat/bidi/
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
# Il campo BIDIOUTLINE numera i paragrafi come i campi AUTONUM/LISTNUM,
# ma è visibile solo quando è abilitata una lingua di editing da destra a sinistra, come l'ebraico o l'arabo.
# Il campo seguente visualizzerà ".1", l'equivalente RTL del numero di elenco "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Aggiungi altri due campi BIDIOUTLINE, che visualizzeranno ".2" e ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Imposta l'allineamento orizzontale del testo per ogni paragrafo nel documento su RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Se abilitiamo una lingua di editing da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno numeri.
# Altrimenti, visualizzeranno "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how to detect plaintext document text direction.

```python
# Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
# per modificare il modo in cui carichiamo un documento di testo semplice.
load_options = aw.loading.TxtLoadOptions()
# Imposta la proprietà "DocumentDirection" su "DocumentDirection.Auto" per rilevare automaticamente
# la direzione di ogni paragrafo di testo che Aspose.Words carica dal testo semplice.
# La proprietà "Bidi" di ogni paragrafo memorizzerà la sua direzione.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Rileva il testo ebraico da destra a sinistra.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Rileva il testo inglese da destra a sinistra.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

