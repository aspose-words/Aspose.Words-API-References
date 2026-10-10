---
title: DocumentBuilder.start_editable_range method
linktitle: start_editable_range method
articleTitle: start_editable_range method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_editable_range method. Marks the current position in the document as an editable range start."
type: docs
weight: 670
url: /ar/python-net/aspose.words/documentbuilder/start_editable_range/
---

## start_editable_range() {#default}

Marks the current position in the document as an editable range start.


```python
def start_editable_range(self):
    ...
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.start_editable_range()](./#default) and [DocumentBuilder.end_editable_range()](../end_editable_range/#default)
or [DocumentBuilder.end_editable_range()](../end_editable_range/#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range start node that was just created.


### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# تسمح النطاقات القابلة للتحرير لنا بترك أجزاء من المستندات المحمية مفتوحة للتحرير.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# النطاق القابل للتحرير المشكل بشكل صحيح يحتوي على عقدة بداية وعقدة نهاية.
# هذه العقد لديها معرفات متطابقة وتحتوي على عقد قابلة للتحرير.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# أجزاء مختلفة من النطاق القابل للتحرير ترتبط ببعضها البعض.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# يمكننا الوصول إلى أنواع العقد لكل جزء هكذا. النطاق القابل للتحرير نفسه ليس عقدة،
# بل كيان يتكون من بداية ونهاية ومحتوياتهما المغلقة.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# أزل نطاقًا قابلًا للتحرير. جميع العقد التي كانت داخل النطاق ستبقى سليمة.
editable_range.remove()
```

Shows how to create nested editable ranges.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " + 'we cannot edit this paragraph without the password.')
# أنشئ نطاقين قابلين للتحرير متداخلين.
outer_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside the outer editable range and can be edited.')
inner_editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph inside both the outer and inner editable ranges and can be edited.')
# حاليًا، مؤشر إدراج العقد في مُنشئ المستند موجود في أكثر من نطاق تحرير جارٍ.
# عندما نرغب في إنهاء نطاق تحرير في هذا الوضع،
# نحتاج إلى تحديد أي من النطاقات نريد إنهاؤه بتمرير عقدة EditableRangeStart الخاصة به.
builder.end_editable_range(inner_editable_range_start)
builder.writeln('This paragraph inside the outer editable range and can be edited.')
builder.end_editable_range(outer_editable_range_start)
builder.writeln('This paragraph is outside any editable ranges, and cannot be edited.')
# إذا كان جزء من النص يحتوي على نطاقين قابلين للتحرير متداخلين مع مجموعات محددة،
# فإن المجموعة المشتركة من المستخدمين المستبعدين من كلا المجموعتين تُمنع من تحريره.
outer_editable_range_start.editable_range.editor_group = aw.EditorType.EVERYONE
inner_editable_range_start.editable_range.editor_group = aw.EditorType.CONTRIBUTORS
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.Nested.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

