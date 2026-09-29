---
title: FootnoteNumberingRule enumeration
linktitle: FootnoteNumberingRule enumeration
articleTitle: FootnoteNumberingRule enumeration
second_title: Aspose.Words for Python
description: "aspose.words.notes.FootnoteNumberingRule enumeration. Determines when automatic footnote or endnote numbering restarts."
type: docs
weight: 40
url: /es/python-net/aspose.words.notes/footnotenumberingrule/
---

## FootnoteNumberingRule enumeration

Determines when automatic footnote or endnote numbering restarts.


### Members

| Name | Description |
| --- | --- |
| CONTINUOUS | Numbering continuous throughout the document. |
| RESTART_SECTION | Numbering restarts at each section. |
| RESTART_PAGE | Numbering restarts at each page. Valid for footnotes only. |
| DEFAULT | Equals [FootnoteNumberingRule.CONTINUOUS](./#CONTINUOUS). |

### Examples

Shows how to restart footnote/endnote numbering at certain places in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Las notas al pie y las notas finales son una forma de adjuntar una referencia o un comentario lateral al texto
# que no interfiere con el flujo del texto principal.
# Insertar una nota al pie/nota final agrega un pequeño símbolo de referencia en superíndice
# en el texto principal donde insertamos la nota al pie/nota final.
# Cada nota al pie/nota final también crea una entrada, que consiste en un símbolo que coincide con la referencia
# símbolo en el texto principal. El texto de referencia que pasamos al método "InsertEndnote" del generador de documentos.
# Las entradas de notas al pie, por defecto, aparecen al final de cada página que contiene
# sus símbolos de referencia, y las notas finales aparecen al final del documento.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# Por defecto, el símbolo de referencia para cada nota al pie y nota final es su índice
# entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
# para notas al pie y notas finales y no reinicia estos recuentos en ningún momento.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# Podemos usar la propiedad "RestartRule" para que el documento se reinicie
# el recuento de notas al pie/notas finales en una nueva página o sección.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

### See Also

* module [aspose.words.notes](../)
* class [FootnoteOptions](../footnoteoptions/)
* class [EndnoteOptions](../endnoteoptions/)

