---
title: FootnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "FootnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered footnotes."
type: docs
weight: 50
url: /es/python-net/aspose.words.notes/footnoteoptions/start_number/
---

## FootnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered footnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [FootnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Las notas al pie y las notas finales son una forma de adjuntar una referencia o un comentario lateral al texto
# que no interfiere con el flujo del texto principal.
# Insertar una nota al pie/nota final agrega un pequeño símbolo de referencia en superíndice
# en el texto principal donde insertamos la nota al pie/nota final.
# Cada nota al pie/nota final también crea una entrada, que consiste en un símbolo
# que coincide con el símbolo de referencia en el texto principal.
# El texto de referencia que pasamos al método "InsertEndnote" del constructor de documentos.
# Las entradas de notas al pie, por defecto, aparecen al final de cada página que contiene
# sus símbolos de referencia, y las notas finales aparecen al final del documento.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# Por defecto, el símbolo de referencia para cada nota al pie y nota final es su índice
# entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
# para notas al pie y para notas finales, que ambas comienzan en 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# Podemos usar la propiedad "StartNumber" para que el documento
# inicie el recuento de una nota al pie o nota final en un número diferente.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

