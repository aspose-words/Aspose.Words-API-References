---
title: StyleType enumeration
linktitle: StyleType enumeration
articleTitle: StyleType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.StyleType enumeration. Represents type of the style."
type: docs
weight: 1260
url: /sv/python-net/aspose.words/styletype/
---

## StyleType enumeration

Represents type of the style.


### Members

| Name | Description |
| --- | --- |
| PARAGRAPH | The style is a paragraph style. |
| CHARACTER | The style is a character style. |
| TABLE | The style is a table style. |
| LIST | The style is a list style. |

### Examples

Shows how to create a list style and use it in a document.

```python
doc = aw.Document()
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Vi kan innehålla ett helt List-objekt inom en stil.
list_style = doc.styles.add(aw.StyleType.LIST, 'MyListStyle')
list1 = list_style.list
self.assertTrue(list1.is_list_style_definition)
self.assertFalse(list1.is_list_style_reference)
self.assertTrue(list1.is_multi_level)
self.assertEqual(list_style, list1.style)
# Ändra utseendet på alla listnivåer i vår lista.
for level in list1.list_levels:
    level.font.name = 'Verdana'
    level.font.color = aspose.pydrawing.Color.blue
    level.font.bold = True
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Using list style first time:')
# Skapa en annan lista från en lista inom en stil.
list2 = doc.lists.add(list_style=list_style)
self.assertFalse(list2.is_list_style_definition)
self.assertTrue(list2.is_list_style_reference)
self.assertEqual(list_style, list2.style)
# Lägg till några listobjekt som vår lista kommer att formatera.
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.writeln('Using list style second time:')
# Skapa och tillämpa en annan lista baserad på liststilen.
list3 = doc.lists.add(list_style=list_style)
builder.list_format.list = list3
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateAndUseListStyle.docx')
```

### See Also

* module [aspose.words](../)

