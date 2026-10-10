---
title: ListCollection class
linktitle: ListCollection class
articleTitle: ListCollection class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListCollection class. Stores and manages formatting of bulleted and numbered lists used in a document"
type: docs
weight: 20
url: /ar/python-net/aspose.words.lists/listcollection/
---

## ListCollection class

Stores and manages formatting of bulleted and numbered lists used in a document.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

A list in a Microsoft Word document is a set of list formatting properties.
The formatting of the lists is stored in the [ListCollection](./) collection separately
from the paragraphs of text.

You do not create objects of this class. There is always only one [ListCollection](./)
object per document and it is accessible via the [DocumentBase.lists](../../aspose.words/documentbase/lists/) property.

To create a new list based on a predefined list template or based on a list style,
use the [ListCollection.add()](./add/#style) method.

To create a new list with formatting identical to an existing list,
use the [ListCollection.add_copy()](./add_copy/#list) method.

To make a paragraph bulleted or numbered, you need to apply list formatting
to a paragraph by assigning a [List](../list/) object to the
[ListFormat.list](../listformat/list/) property of [ListFormat](../listformat/).

To remove list formatting from a paragraph, use the [ListFormat.remove_numbers()](../listformat/remove_numbers/#default)
method.

If you know a bit about WordprocessingML, then you might know it defines separate concepts
for "list" and "list definition". This exactly corresponds to how list formatting is stored
in a Microsoft Word document at the low level. List definition is like a "schema" and
list is like an instance of a list definition.

To simplify programming model, Aspose.Words hides the distinction between list and list
definition in much the same way like Microsoft Word hides this in its user interface.
This allows you to concentrate more on how you want your document to look like, rather than
building low-level objects to satisfy requirements of the Microsoft Word file format.

It is not possible to delete lists once they are created in the current version of Aspose.Words.
This is similar to Microsoft Word where user does not have explicit control over list definitions.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a list by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the count of numbered and bulleted lists in the document. |
| [document](./document/) | Gets the owner document. |

### Methods

| Name | Description |
| --- | --- |
|[ add(list_template)](./add/#listtemplate) | Creates a new list based on a predefined template and adds it to the collection of lists in the document. |
|[ add(list_style)](./add/#style) | Creates a new list that references a list style and adds it to the collection of lists in the document. |
|[ add_copy(src_list)](./add_copy/#list) | Creates a new list by copying the specified list and adding it to the collection of lists in the document. |
|[ add_single_level_list(list_template)](./add_single_level_list/#listtemplate) | Creates a new single level list based on the predefined template and adds it to the list collection in the document. |
|[ get_list_by_list_id(list_id)](./get_list_by_list_id/#int) | Gets a list by a list identifier. |

### Examples

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام مُنشئ المستند.
# 1 -  قائمة مرقمة:
# القوائم المرقمة تُنشئ ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# عن طريق ضبط خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
# لبدء قائمة فرعية مستقلة عند العنصر الحالي في القائمة.
# قالب قائمة Microsoft Word المسمى "NumberDefault" يستخدم الأرقام لإنشاء مستويات القائمة للمستوى الأول.
# المستويات الأعمق للقائمة تستخدم الأحرف والأرقام الرومانية الصغيرة.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  قائمة نقطية:
# هذه القائمة ستضيف مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
# المستويات الأعمق لهذه القائمة ستستخدم رموزًا مختلفة، مثل "■" و "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# يمكننا تعطيل تنسيق القوائم لتجنب تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين العلم "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# القائمة تتيح لنا تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
# يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
# يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لمُنشئ المستند.
# كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
# إنشاء قائمة من قالب Microsoft Word، وتخصيص المستوى الأول من القائمة.
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# تطبيق قائمتنا على بعض الفقرات.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قوائم المستند
# لإنشاء قائمة مشابهة دون تعديل الأصل.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# تطبيق القائمة الثانية على فقرات جديدة.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

Shows how to create a document with a sample of all the lists from another document.

```python
src_doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
for src_list in src_doc.lists:
    dst_list = dst_doc.lists.add_copy(src_list)
    ExLists._add_list_sample(builder, dst_list)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Lists.PrintOutAllLists.docx')
```

Shows how to create a document with a sample of all the lists from another document (AddListSample).

```python
@staticmethod
def _add_list_sample(builder, doc_list):
    builder.writeln('Sample formatting of list with ListId:' + str(doc_list.list_id))
    builder.list_format.list = doc_list
    i = 0
    while i < doc_list.list_levels.count:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    builder.list_format.remove_numbers()
    builder.writeln()
```

### See Also

* module [aspose.words.lists](../)
* class [List](../list/)
* class [ListLevel](../listlevel/)
* class [ListFormat](../listformat/)

