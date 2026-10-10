---
title: ListCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListCollection.add method"
type: docs
weight: 40
url: /sv/python-net/aspose.words.lists/listcollection/add/
---

## add(list_template) {#listtemplate}

Creates a new list based on a predefined template and adds it to the collection of lists in the document.


```python
def add(self, list_template: aspose.words.lists.ListTemplate):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_template | [ListTemplate](../../listtemplate/) | The template of the list. |

### Remarks

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.

All lists created using this method have 9 list levels.




### Returns

The newly created list.


## add(list_style) {#style}

Creates a new list that references a list style and adds it to the collection of lists in the document.


```python
def add(self, list_style: aspose.words.Style):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_style | [Style](../../../aspose.words/style/) | The list style. |

### Remarks

The newly created list references the list style. If you change the properties of the list
style, it is reflected in the properties of the list. Vice versa, if you change the properties
of the list, it is reflected in the properties of the list style.




### Returns

The newly created list.


## Examples

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

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Applicera vår lista på några stycken.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# Vi kan lägga till en kopia av en befintlig lista till dokumentets listsamling
# för att skapa en liknande lista utan att ändra originalet.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Applicera den andra listan på nya stycken.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

Shows how to create a list by applying a new list format to a collection of paragraphs.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1')
builder.writeln('Paragraph 2')
builder.write('Paragraph 3')
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_UPPERCASE_LETTER_DOT)
for paragraph in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras))):
    paragraph.list_format.list = doc_list
    paragraph.list_format.list_level_number = 1
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

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

## See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

