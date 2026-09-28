---
title: Font.name_other property
linktitle: name_other property
articleTitle: name_other property
second_title: Aspose.Words for Python
description: "Font.name_other property. Returns or sets the font used for characters with character codes from 128 through 255."
type: docs
weight: 270
url: /ar/python-net/aspose.words/font/name_other/
---

## Font.name_other property

Returns or sets the font used for characters with character codes from 128 through 255.


```python
@property
def name_other(self) -> str:
    ...

@name_other.setter
def name_other(self, value: str):
    ...

```

### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# افترض وجود مقطع نستخدم المنشئ لإدراجه أثناء استخدام تكوين الخط هذا
# يحتوي على أحرف ضمن نطاق أحرف ASCII. في هذه الحالة،
# سيعرض تلك الأحرف باستخدام هذا الخط.
builder.font.name_ascii = 'Calibri'
# في حال عدم تحديد خط آخر، سيطبق المُنشئ هذا الخط على جميع الأحرف التي يُدرجها.
self.assertEqual('Calibri', builder.font.name)
# حدد خطًا لاستخدامه لجميع الأحرف خارج نطاق ASCII.
# من الناحية المثالية، يجب أن يحتوي هذا الخط على رمز لكل رمز حرف غير ASCII مطلوب.
builder.font.name_other = 'Courier New'
# أدرج تشغيلًا يحتوي على كلمة واحدة مكوّنة من أحرف ASCII، وكلمة أخرى تحتوي على جميع الأحرف خارج ذلك النطاق.
# سيتم عرض كل حرف باستخدام أحد الخطين، حسب.
builder.writeln('Hello, Привет')
doc.save(file_name=ARTIFACTS_DIR + 'Font.NameAscii.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

