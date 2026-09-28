---
title: CleanupOptions.unused_lists property
linktitle: unused_lists property
articleTitle: unused_lists property
second_title: Aspose.Words for Python
description: "CleanupOptions.unused_lists property. Specifies whether unused list and list definitions should be removed from document"
type: docs
weight: 40
url: /ar/python-net/aspose.words/cleanupoptions/unused_lists/
---

## CleanupOptions.unused_lists property

Specifies whether unused list and list definitions should be removed from document.
Default value is ``True``.



```python
@property
def unused_lists(self) -> bool:
    ...

@unused_lists.setter
def unused_lists(self, value: bool):
    ...

```

### Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# مُدمَجًا مع الأنماط المدمجة، يحتوي المستند الآن على ثمانية أنماط.
# يُعلَّم النمط المخصص بأنه "مستخدم" طالما يوجد أي نص داخل المستند
# مُنسَّقًا بهذا النمط. هذا يعني أن الأنماط الأربعة التي أضفناها غير مستخدمة حاليًا.
self.assertEqual(8, doc.styles.count)
# طبق نمط حرف مخصص، ثم نمط قائمة مخصص. سيؤدي ذلك إلى تعليمها بأنها "مستخدمة".
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# الآن، هناك نمط حرف غير مستخدم ونمط قائمة غير مستخدم.
# طريقة Cleanup()، عندما تُكوَّن باستخدام كائن CleanupOptions، يمكنها استهداف الأنماط غير المستخدمة وإزالتها.
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# إزالة كل عقدة يُطبق عليها نمط مخصص سيعيد تعليمها بأنها "غير مستخدمة" مرة أخرى.
# أعد تشغيل طريقة Cleanup لإزالتها.
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

