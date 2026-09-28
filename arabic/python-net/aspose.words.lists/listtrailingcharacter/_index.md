---
title: ListTrailingCharacter enumeration
linktitle: ListTrailingCharacter enumeration
articleTitle: ListTrailingCharacter enumeration
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListTrailingCharacter enumeration. Specifies the character that separates the list label from the text of the paragraph."
type: docs
weight: 90
url: /ar/python-net/aspose.words.lists/listtrailingcharacter/
---

## ListTrailingCharacter enumeration

Specifies the character that separates the list label from the text of the paragraph.

Used as a value for the [ListLevel.trailing_character](../listlevel/trailing_character/) property.




### Members

| Name | Description |
| --- | --- |
| TAB | A tab character is placed between the list label and text of the paragraph. |
| SPACE | A space character is placed between the list label and text of the paragraph. |
| NOTHING | There is no separator character between the list label and text of the paragraph. |

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# إنشاء قائمة من قالب Microsoft Word، وتخصيص أول مستويين من مستويات القائمة.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# قيمة NumberFormat هذه ستُنشئ رموزًا نقطية على شكل نجمة.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# إنشاء فقرات وتطبيق كلا مستويي القائمة من تنسيق قائمتنا المخصص عليها.
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

### See Also

* module [aspose.words.lists](../)

