---
title: Style.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "Style.name property. Gets or sets the name of the style."
type: docs
weight: 130
url: /ar/python-net/aspose.words/style/name/
---

## Style.name property

Gets or sets the name of the style.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.




### Examples

Shows how to access a document's style collection.

```python
doc = aw.Document()
self.assertEqual(4, doc.styles.count)
# عدّ وسرد جميع الأنماط التي يحتويها مستند تم إنشاؤه باستخدام Aspose.Words بشكل افتراضي.
for cur_style in doc.styles:
    print(f'Style name:\t"{cur_style.name}", of type "{cur_style.type}"')
    print(f'\tSubsequent style:\t{cur_style.next_paragraph_style_name}')
    print(f'\tIs heading:\t\t\t{cur_style.is_heading}')
    print(f'\tIs QuickStyle:\t\t{cur_style.is_quick_style}')
    self.assertEqual(doc, cur_style.document)
```

Shows how to clone a document's style.

```python
doc = aw.Document()
# طريقة AddCopy تنشئ نسخة من النمط المحدد و
# تولد تلقائياً اسمًا جديدًا للنمط، مثل "Heading 1_0".
new_style = doc.styles.add_copy(doc.styles.get_by_name('Heading 1'))
# استخدم خاصية "Name" للنمط لتغيير الاسم التعريفي للنمط.
new_style.name = 'My Heading 1'
# المستند الآن يحتوي على نمطين مظهرهما متطابق بأسماء مختلفة.
# تغيير إعدادات أحد الأنماط لا يؤثر على الآخر.
new_style.font.color = aspose.pydrawing.Color.red
self.assertEqual('My Heading 1', new_style.name)
self.assertEqual('Heading 1', doc.styles.get_by_name('Heading 1').name)
self.assertEqual(doc.styles.get_by_name('Heading 1').type, new_style.type)
self.assertEqual(doc.styles.get_by_name('Heading 1').font.name, new_style.font.name)
self.assertEqual(doc.styles.get_by_name('Heading 1').font.size, new_style.font.size)
self.assertNotEqual(doc.styles.get_by_name('Heading 1').font.color, new_style.font.color)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

