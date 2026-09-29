---
title: ListTemplate enumeration
linktitle: ListTemplate enumeration
articleTitle: ListTemplate enumeration
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListTemplate enumeration. Specifies one of the predefined list formats available in Microsoft Word."
type: docs
weight: 80
url: /sv/python-net/aspose.words.lists/listtemplate/
---

## ListTemplate enumeration

Specifies one of the predefined list formats available in Microsoft Word.

A list template value is used as a parameter into the
[ListCollection.add()](../listcollection/add/#listtemplate) method.

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.




### Members

| Name | Description |
| --- | --- |
| BULLET_DEFAULT | Default bulleted list with 9 levels. Bullet of the first level is a disc, bullet of the second level is a circle, bullet of the third level is a square. Then formatting repeats for the remaining levels. |
| BULLET_DISK | Same as [ListTemplate.BULLET_DEFAULT](./#BULLET_DEFAULT). |
| BULLET_CIRCLE | The bullet of the first level is a circle. The remaining levels are same as in [ListTemplate.BULLET_DEFAULT](./#BULLET_DEFAULT). |
| BULLET_SQUARE | The bullet of the first level is a square. The remaining levels are same as in [ListTemplate.BULLET_DEFAULT](./#BULLET_DEFAULT). |
| BULLET_DIAMONDS | The bullet of the first level is a 4-diamond Wingding character. The remaining levels are same as in [ListTemplate.BULLET_DEFAULT](./#BULLET_DEFAULT). |
| BULLET_ARROW_HEAD | The bullet of the first level is an arrow head Wingding character. The remaining levels are same as in [ListTemplate.BULLET_DEFAULT](./#BULLET_DEFAULT). |
| BULLET_TICK | The bullet of the first level is a tick Wingding character. The remaining levels are same as in [ListTemplate.BULLET_DEFAULT](./#BULLET_DEFAULT). |
| NUMBER_DEFAULT | Default numbered list with 9 levels. Arabic numbering (1., 2., 3., ...) for the first level, lowercase letter numbering (a., b., c., ...) for the second level, lowercase roman numbering (i., ii., iii., ...) for the third level. Then formatting repeats for the remaining levels. |
| NUMBER_ARABIC_DOT | Same as [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| NUMBER_ARABIC_PARENTHESIS | The number of the first level is "1)". The remaining levels are same as in [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| NUMBER_UPPERCASE_ROMAN_DOT | The number of the first level is "I.". The remaining levels are same as in [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| NUMBER_UPPERCASE_LETTER_DOT | The number of the first level is "A.". The remaining levels are same as in [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| NUMBER_LOWERCASE_LETTER_PARENTHESIS | The number of the first level is "a)". The remaining levels are same as in [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| NUMBER_LOWERCASE_LETTER_DOT | The number of the first level is "a.". The remaining levels are same as in [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| NUMBER_LOWERCASE_ROMAN_DOT | The number of the first level is "i.". The remaining levels are same as in [ListTemplate.NUMBER_DEFAULT](./#NUMBER_DEFAULT). |
| OUTLINE_NUMBERS | An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.". |
| OUTLINE_LEGAL | An outline list with levels are numbered "1., 1.1., 1.1.1, ...". |
| OUTLINE_BULLETS | An outline lists with various bullets for different levels. |
| OUTLINE_HEADINGS_ARTICLE_SECTION | An outline list with levels linked to Heading styles. |
| OUTLINE_HEADINGS_LEGAL | An outline list with levels linked to Heading styles. |
| OUTLINE_HEADINGS_NUMBERS | An outline list with levels linked to Heading styles. |
| OUTLINE_HEADINGS_CHAPTER | An outline list with levels linked to Heading styles. |

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

Shows how to create a document that contains all outline headings list templates.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_HEADINGS_ARTICLE_SECTION)
ExLists._add_outline_heading_paragraphs(builder, doc_list, 'Aspose.Words Outline - "Article Section"')
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_HEADINGS_LEGAL)
ExLists._add_outline_heading_paragraphs(builder, doc_list, 'Aspose.Words Outline - "Legal"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_HEADINGS_NUMBERS)
ExLists._add_outline_heading_paragraphs(builder, doc_list, 'Aspose.Words Outline - "Numbers"')
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_HEADINGS_CHAPTER)
ExLists._add_outline_heading_paragraphs(builder, doc_list, 'Aspose.Words Outline - "Chapters"')
doc.save(file_name=ARTIFACTS_DIR + 'Lists.OutlineHeadingTemplates.docx')
```

Shows how to create a document that contains all outline headings list templates (AddOutlineHeadingParagraphs).

```python
@staticmethod
def _add_outline_heading_paragraphs(builder, doc_list, title):
    builder.paragraph_format.clear_formatting()
    builder.writeln(title)
    i = 0
    while i < 9:
        builder.list_format.list = doc_list
        builder.list_format.list_level_number = i
        style_name = 'Heading ' + str(i + 1)
        builder.paragraph_format.style_name = style_name
        builder.writeln(style_name)
        i += 1
    builder.list_format.remove_numbers()
```

### See Also

* module [aspose.words.lists](../)

