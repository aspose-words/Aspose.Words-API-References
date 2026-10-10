---
title: List.is_multi_level property
linktitle: is_multi_level property
articleTitle: is_multi_level property
second_title: Aspose.Words for Python
description: "List.is_multi_level property. Returns ``True`` when the list contains 9 levels; ``False`` when 1 level."
type: docs
weight: 40
url: /sv/python-net/aspose.words.lists/list/is_multi_level/
---

## List.is_multi_level property

Returns ``True`` when the list contains 9 levels; ``False`` when 1 level.



```python
@property
def is_multi_level(self) -> bool:
    ...

```

### Remarks

The lists that you create with Aspose.Words are always multi-level lists and contain 9 levels.

Microsoft Word 2003 and later always create multi-level lists with 9 levels.
But in some documents, created with earlier versions of Microsoft Word you might encounter
lists that have 1 level only.




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

* module [aspose.words.lists](../../)
* class [List](../)

