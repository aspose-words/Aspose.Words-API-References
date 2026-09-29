---
title: ListFormat.list property
linktitle: list property
articleTitle: list property
second_title: Aspose.Words for Python
description: "ListFormat.list property. Gets or sets the list this paragraph is a member of."
type: docs
weight: 20
url: /sv/python-net/aspose.words.lists/listformat/list/
---

## ListFormat.list property

Gets or sets the list this paragraph is a member of.


```python
@property
def list(self) -> aspose.words.lists.List:
    ...

@list.setter
def list(self, value: aspose.words.lists.List):
    ...

```

### Remarks

The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to ``None`` removes bullets and numbering from the paragraph
and sets the list level number to zero. Setting this property to ``None`` is equivalent
to calling [ListFormat.remove_numbers()](../remove_numbers/#default).




### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Nedan är två typer av listor som vi kan skapa med en dokumentbyggare.
# 1 -  En numrerad lista:
# Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Genom att sätta egenskapen "ListLevelNumber" kan vi öka listnivån
# för att börja en självständig underlista vid det aktuella listobjektet.
# Microsoft Word-listmallen som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
# Djupare listnivåer använder bokstäver och gemena romerska siffror.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  En punktlista:
# Denna lista kommer att applicera ett indrag och en punktmarkör ("•") före varje stycke.
# Djupare nivåer i denna lista kommer att använda olika symboler, såsom "■" och "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Vi kan inaktivera listformatering för att inte formatera efterföljande stycken som listor genom att avaktivera flaggan "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

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

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list_level_number](../list_level_number/)
* method [ListFormat.remove_numbers()](../remove_numbers/#default)

