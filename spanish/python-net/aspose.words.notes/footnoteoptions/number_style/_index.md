---
title: FootnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "FootnoteOptions.number_style property. Specifies the number format for automatically numbered footnotes."
type: docs
weight: 20
url: /es/python-net/aspose.words.notes/footnoteoptions/number_style/
---

## FootnoteOptions.number_style property

Specifies the number format for automatically numbered footnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

