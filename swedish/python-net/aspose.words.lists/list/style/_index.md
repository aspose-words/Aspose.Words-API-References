---
title: List.style property
linktitle: style property
articleTitle: style property
second_title: Aspose.Words for Python
description: "List.style property. Gets the list style that this list references or defines."
type: docs
weight: 80
url: /sv/python-net/aspose.words.lists/list/style/
---

## List.style property

Gets the list style that this list references or defines.


```python
@property
def style(self) -> aspose.words.Style:
    ...

```

### Remarks

If this list is not associated with a list style, the property will return ``None``.

A list could be a reference to a list style, in this case [List.is_list_style_reference](../is_list_style_reference/)
will be ``True``.

A list could be a definition of a list style, in this case [List.is_list_style_definition](../is_list_style_definition/)
will be ``True``. Such a list cannot be applied to paragraphs in the document directly.




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

