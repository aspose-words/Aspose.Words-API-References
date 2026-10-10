---
title: TxtLoadOptions.detect_numbering_with_whitespaces property
linktitle: detect_numbering_with_whitespaces property
articleTitle: detect_numbering_with_whitespaces property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.detect_numbering_with_whitespaces property. Allows to specify how numbered list items are recognized when document is imported from plain text format"
type: docs
weight: 40
url: /ar/python-net/aspose.words.loading/txtloadoptions/detect_numbering_with_whitespaces/
---

## TxtLoadOptions.detect_numbering_with_whitespaces property

Allows to specify how numbered list items are recognized when document is imported from plain text format.
The default value is ``True``.


```python
@property
def detect_numbering_with_whitespaces(self) -> bool:
    ...

@detect_numbering_with_whitespaces.setter
def detect_numbering_with_whitespaces(self, value: bool):
    ...

```

### Remarks

If this option is set to ``False``, lists recognition algorithm detects list paragraphs, when list numbers ends with
either dot, right bracket or bullet symbols (such as "•", "\*", "-" or "o").

If this option is set to ``True``, whitespaces are also used as list number delimiters:
list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.




### Examples

Shows how to detect lists when loading plaintext documents.

```python
# أنشئ مستند نص عادي في سلسلة يحتوي على أربعة أجزاء منفصلة يمكننا تفسيرها كقوائم،
# مع فواصل مختلفة. عند تحميل المستند النصي إلى كائن \"Document\"،
# ستقوم Aspose.Words دائمًا باكتشاف القوائم الثلاث الأولى وستضيف كائن \"List\"
# لكل منها إلى خاصية \"Lists\" في المستند.
text_doc = 'Full stop delimiters:\n' + '1. First list item 1\n' + '2. First list item 2\n' + '3. First list item 3\n\n' + 'Right bracket delimiters:\n' + '1) Second list item 1\n' + '2) Second list item 2\n' + '3) Second list item 3\n\n' + 'Bullet delimiters:\n' + '• Third list item 1\n' + '• Third list item 2\n' + '• Third list item 3\n\n' + 'Whitespace delimiters:\n' + '1 Fourth list item 1\n' + '2 Fourth list item 2\n' + '3 Fourth list item 3'
# أنشئ كائن "TxtLoadOptions"، الذي يمكننا تمريره إلى مُنشئ المستند
# لتعديل طريقة تحميل مستند نص عادي.
load_options = aw.loading.TxtLoadOptions()
# قم بتعيين خاصية \"DetectNumberingWithWhitespaces\" إلى \"true\" لاكتشاف العناصر المرقمة
# مع فواصل مسافات بيضاء، مثل القائمة الرابعة في مستندنا، كقوائم.
# قد يؤدي ذلك أيضًا إلى اكتشاف الفقرات التي تبدأ بأرقام كقوائم عن طريق الخطأ.
# قم بتعيين خاصية \"DetectNumberingWithWhitespaces\" إلى \"false\"
# لعدم إنشاء قوائم من العناصر المرقمة ذات فواصل المسافات البيضاء.
load_options.detect_numbering_with_whitespaces = detect_numbering_with_whitespaces
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(text_doc, system_helper.text.Encoding.utf_8())), load_options=load_options)
if detect_numbering_with_whitespaces:
    self.assertEqual(4, doc.lists.count)
    self.assertTrue(any(['Fourth list' in p.get_text() and p.as_paragraph().is_list_item for p in doc.first_section.body.paragraphs]))
else:
    self.assertEqual(3, doc.lists.count)
    self.assertFalse(any(['Fourth list' in p.get_text() and p.as_paragraph().is_list_item for p in doc.first_section.body.paragraphs]))
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

