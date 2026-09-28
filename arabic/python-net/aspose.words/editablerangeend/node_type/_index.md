---
title: EditableRangeEnd.node_type property
linktitle: node_type property
articleTitle: node_type property
second_title: Aspose.Words for Python
description: "EditableRangeEnd.node_type property. Returns [NodeType.EDITABLE_RANGE_END](../../nodetype/#EDITABLE_RANGE_END)."
type: docs
weight: 30
url: /ar/python-net/aspose.words/editablerangeend/node_type/
---

## EditableRangeEnd.node_type property

Returns [NodeType.EDITABLE_RANGE_END](../../nodetype/#EDITABLE_RANGE_END).



```python
@property
def node_type(self) -> aspose.words.NodeType:
    ...

```

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

### See Also

* module [aspose.words](../../)
* class [EditableRangeEnd](../)

