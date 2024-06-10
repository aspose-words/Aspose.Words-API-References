---
title: ListTemplate enumeration
linktitle: ListTemplate enumeration
articleTitle: ListTemplate enumeration
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListTemplate enumeration. Specifies one of the predefined list formats available in Microsoft Word."
type: docs
weight: 80
url: /python-net/aspose.words.lists/listtemplate/
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
builder = aw.DocumentBuilder(doc)
self.assertFalse(builder.list_format.is_list_item)
# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Below are two types of lists that we can create using a document builder.
# 1 -  A numbered list:
# Numbered lists create a logical order for their paragraphs by numbering each item.
builder.list_format.list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# By setting the "list_level_number" property, we can increase the list level
# to begin a self-contained sub-list at the current list item.
# The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
# Deeper list levels use letters and lowercase Roman numerals.
for i in range(9):
    builder.list_format.list_level_number = i
    builder.writeln(f'Level {i}')
# 2 -  A bulleted list:
# This list will apply an indent and a bullet symbol ("•") before each paragraph.
# Deeper levels of this list will use different symbols, such as "■" and "○".
builder.list_format.list = doc.lists.add(aw.lists.ListTemplate.BULLET_DEFAULT)
for i in range(9):
    builder.list_format.list_level_number = i
    builder.writeln(f'Level {i}')
# We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(ARTIFACTS_DIR + 'Lists.specify_list_level.docx')
```

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Create a list from a Microsoft Word template, and customize its first list level.
list1 = doc.lists.add(aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Apply our list to some paragraphs.
builder = aw.DocumentBuilder(doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# We can add a copy of an existing list to the document's list collection
# to create a similar list without making changes to the original.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Apply the second list to new paragraphs.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(ARTIFACTS_DIR + 'Lists.restart_numbering_using_list_copy.docx')
```

Shows how to create a document that contains all outline headings list templates.

```python
def outline_heading_templates():
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    list_ = doc.lists.add(aw.lists.ListTemplate.OUTLINE_HEADINGS_ARTICLE_SECTION)
    add_outline_heading_paragraphs(builder, list_, 'Aspose.Words Outline - "Article Section"')
    list_ = doc.lists.add(aw.lists.ListTemplate.OUTLINE_HEADINGS_LEGAL)
    add_outline_heading_paragraphs(builder, list_, 'Aspose.Words Outline - "Legal"')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    list_ = doc.lists.add(aw.lists.ListTemplate.OUTLINE_HEADINGS_NUMBERS)
    add_outline_heading_paragraphs(builder, list_, 'Aspose.Words Outline - "Numbers"')
    list_ = doc.lists.add(aw.lists.ListTemplate.OUTLINE_HEADINGS_CHAPTER)
    add_outline_heading_paragraphs(builder, list_, 'Aspose.Words Outline - "Chapters"')
    doc.save(ARTIFACTS_DIR + 'Lists.outline_heading_templates.docx')

def add_outline_heading_paragraphs(builder: aw.DocumentBuilder, list: aw.lists.List, title: str):
    builder.paragraph_format.clear_formatting()
    builder.writeln(title)
    for i in range(9):
        builder.list_format.list = list
        builder.list_format.list_level_number = i
        style_name = f'Heading {i + 1}'
        builder.paragraph_format.style_name = style_name
        builder.writeln(style_name)
    builder.list_format.remove_numbers()
```

### See Also

* module [aspose.words.lists](../)

