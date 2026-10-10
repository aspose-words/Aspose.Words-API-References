---
title: FindReplaceOptions.smart_paragraph_break_replacement property
linktitle: smart_paragraph_break_replacement property
articleTitle: smart_paragraph_break_replacement property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.smart_paragraph_break_replacement property. Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph."
type: docs
weight: 180
url: /fr/python-net/aspose.words.replacing/findreplaceoptions/smart_paragraph_break_replacement/
---

## FindReplaceOptions.smart_paragraph_break_replacement property

Gets or sets a boolean value indicating either it is allowed to replace paragraph break
when there is no next sibling paragraph.

The default value is ``False``.




```python
@property
def smart_paragraph_break_replacement(self) -> bool:
    ...

@smart_paragraph_break_replacement.setter
def smart_paragraph_break_replacement(self, value: bool):
    ...

```

### Remarks

This option allows to replace paragraph break when there is no next sibling paragraph to which all child
nodes can be moved, by finding any (not necessarily sibling) next paragraph after the paragraph being replaced.


### Examples

Shows how to remove paragraph from a table cell with a nested table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez un tableau avec un paragraphe et un tableau interne dans la première cellule.
builder.start_table()
builder.insert_cell()
builder.write('TEXT1')
builder.start_table()
builder.insert_cell()
builder.end_table()
builder.end_table()
builder.writeln()
options = aw.replacing.FindReplaceOptions()
# Lorsque l'option suivante est définie sur 'true', Aspose.Words supprimera le texte du paragraphe
# complètement avec sa marque de paragraphe. Sinon, Aspose.Words imitera Word et supprimera
# seulement le texte du paragraphe et laissera la marque de paragraphe intacte (lorsqu'un tableau suit le texte).
options.smart_paragraph_break_replacement = is_smart_paragraph_break_replacement
doc.range.replace_regex(pattern='TEXT1&p', replacement='', options=options)
doc.save(file_name=ARTIFACTS_DIR + 'Table.RemoveParagraphTextAndMark.docx')
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

