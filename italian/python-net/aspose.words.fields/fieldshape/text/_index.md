---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/fieldshape/text/
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

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Apri un documento creato in Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Se apriamo il documento Word e premiamo Alt+F9, vedremo un campo SHAPE e un campo EMBED.
# Un campo SHAPE è l'ancora/tela per un oggetto AutoShape con lo stile di avvolgimento "In linea con il testo" abilitato.
# Un campo EMBED ha la stessa funzione, ma per un oggetto incorporato,
# come un foglio di calcolo da un documento Excel esterno.
# Tuttavia, questi campi non appariranno nella collezione Fields del documento.
self.assertEqual(0, doc.range.fields.count)
# Questi campi sono supportati solo dalle versioni vecchie di Microsoft Word.
# Il processo di caricamento del documento convertirà questi campi in oggetti Shape,
# che possiamo accedere nella collezione di nodi del documento.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# Il primo nodo Shape corrisponde al campo SHAPE nel documento di input,
# che è la tela in linea per l'AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# Il secondo nodo Shape è l'AutoShape stessa.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Il terzo Shape è quello che era il campo EMBED che conteneva il foglio di calcolo esterno.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

