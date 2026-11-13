---
title: Document.endnote_options property
linktitle: endnote_options property
articleTitle: endnote_options property
second_title: Aspose.Words for Python
description: "Document.endnote_options property. Provides options that control numbering and positioning of endnotes in this document."
type: docs
weight: 120
url: /es/python-net/aspose.words/document/endnote_options/
---

## Document.endnote_options property

Provides options that control numbering and positioning of endnotes in this document.


```python
@property
def endnote_options(self) -> aspose.words.notes.EndnoteOptions:
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Una nota al final es una forma de adjuntar una referencia o un comentario lateral al texto
# que no interfiere con el flujo del texto principal.
# Insertar una nota al final agrega un pequeño símbolo de referencia en superíndice
# en el texto principal donde insertamos la nota al final.
# Cada nota al final también crea una entrada al final del documento, que consiste en un símbolo
# que coincide con el símbolo de referencia en el texto principal.
# El texto de referencia que pasamos al método "InsertEndnote" del constructor de documentos.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# Podemos usar la propiedad "Position" para determinar dónde el documento colocará todas sus notas al final.
# Si establecemos el valor de la propiedad "Position" a "EndnotePosition.EndOfDocument",
# Cada nota al pie aparecerá en una colección al final del documento. Este es el valor predeterminado.
# Si establecemos el valor de la propiedad "Position" a "EndnotePosition.EndOfSection",
# cada nota al pie aparecerá en una colección al final de la sección cuyo texto contiene la marca de referencia de la nota final.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

Shows how to change the number style of footnote/endnote reference marks.

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
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# Por defecto, el símbolo de referencia para cada nota al pie y nota final es su índice
# entre todas las notas al pie/notas finales del documento. Cada documento mantiene recuentos separados
# para notas al pie y para notas finales. Por defecto, las notas al pie muestran sus números usando numerales arábigos,
# y las notas finales muestran sus números en numerales romanos en minúscula.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# Podemos usar la propiedad "NumberStyle" para aplicar estilos de numeración personalizados a las notas al pie y notas finales.
# Esto no afectará a las notas al pie/notas finales con marcas de referencia personalizadas.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

