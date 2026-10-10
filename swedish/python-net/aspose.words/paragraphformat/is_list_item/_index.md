---
title: ParagraphFormat.is_list_item property
linktitle: is_list_item property
articleTitle: is_list_item property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_list_item property. True when the paragraph is an item in a bulleted or numbered list."
type: docs
weight: 150
url: /sv/python-net/aspose.words/paragraphformat/is_list_item/
---

## ParagraphFormat.is_list_item property

True when the paragraph is an item in a bulleted or numbered list.


```python
@property
def is_list_item(self) -> bool:
    ...

```

### Examples

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Skapa en dispositionslista för rubrikerna.
outline_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 1')
# Skapa en numrerad lista.
numbered_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Numbered list item 1.')
# Varje stycke som utgör en lista kommer att ha denna flagga.
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)
# Skapa en punktlista.
bulleted_list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln('Bulleted list item 1.')
builder.writeln('Bulleted list item 2.')
builder.paragraph_format.clear_formatting()
# Återgå till den numrerade listan.
builder.list_format.list = numbered_list
builder.writeln('Numbered list item 2.')
builder.writeln('Numbered list item 3.')
# Återgå till dispositionslistan.
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 2')
builder.paragraph_format.clear_formatting()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.NestedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

