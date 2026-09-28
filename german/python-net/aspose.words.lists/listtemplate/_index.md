---
title: ListTemplate enumeration
linktitle: ListTemplate enumeration
articleTitle: ListTemplate enumeration
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListTemplate enumeration. Specifies one of the predefined list formats available in Microsoft Word."
type: docs
weight: 80
url: /de/python-net/aspose.words.lists/listtemplate/
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
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
# Unten sind zwei Listentypen, die wir mit einem Document Builder erstellen können.
# 1 -  Eine nummerierte Liste:
# Nummerierte Listen erzeugen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Durch das Setzen der "ListLevelNumber"-Eigenschaft können wir die Listenebene erhöhen
# um eine eigenständige Unterliste beim aktuellen Listenelement zu beginnen.
# Die Microsoft‑Word-Listenvorlage mit dem Namen "NumberDefault" verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
# Tiefere Listenebenen verwenden Buchstaben und kleinbuchstabige römische Ziffern.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Eine Aufzählungsliste:
# Diese Liste wird vor jedem Absatz einen Einzug und ein Aufzählungssymbol ("•") anwenden.
# Tiefere Ebenen dieser Liste verwenden unterschiedliche Symbole, wie "■" und "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Wir können die Listformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das "List"-Flag zurücksetzen.
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
# Erstellen Sie eine Liste aus einer Microsoft‑Word-Vorlage und passen Sie deren erste Listenebene an.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Wenden Sie unsere Liste auf einige Absätze an.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# Wir können eine Kopie einer bestehenden Liste zur Listensammlung des Dokuments hinzufügen
# um eine ähnliche Liste zu erstellen, ohne das Original zu ändern.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Wenden Sie die zweite Liste auf neue Absätze an.
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

