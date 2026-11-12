---
title: EditableRangeStart.editable_range property
linktitle: editable_range property
articleTitle: editable_range property
second_title: Aspose.Words for Python
description: "EditableRangeStart.editable_range property. Gets the facade object that encapsulates this editable range start and end."
type: docs
weight: 10
url: /ru/python-net/aspose.words/editablerangestart/editable_range/
---

## EditableRangeStart.editable_range property

Gets the facade object that encapsulates this editable range start and end.


```python
@property
def editable_range(self) -> aspose.words.EditableRange:
    ...

```

### Examples

Shows how to work with an editable range.

```python
doc = aw.Document()
doc.protect(type=aw.ProtectionType.READ_ONLY, password='MyPassword')
builder = aw.DocumentBuilder(doc=doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only," + ' we cannot edit this paragraph without the password.')
# Редактируемые диапазоны позволяют оставлять части защищённых документов открытыми для редактирования.
editable_range_start = builder.start_editable_range()
builder.writeln('This paragraph is inside an editable range, and can be edited.')
editable_range_end = builder.end_editable_range()
# Корректно сформированный редактируемый диапазон имеет начальный и конечный узлы.
# Эти узлы имеют совпадающие идентификаторы и охватывают редактируемые узлы.
editable_range = editable_range_start.editable_range
self.assertEqual(editable_range_start.id, editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.id)
# Разные части редактируемого диапазона связаны друг с другом.
self.assertEqual(editable_range_start.id, editable_range.editable_range_start.id)
self.assertEqual(editable_range_start.id, editable_range_end.editable_range_start.id)
self.assertEqual(editable_range.id, editable_range_start.editable_range.id)
self.assertEqual(editable_range_end.id, editable_range.editable_range_end.id)
# Мы можем получить типы узлов каждой части следующим образом. Сам редактируемый диапазон не является узлом,
# а является сущностью, состоящей из начала, конца и их вложенного содержимого.
self.assertEqual(aw.NodeType.EDITABLE_RANGE_START, editable_range_start.node_type)
self.assertEqual(aw.NodeType.EDITABLE_RANGE_END, editable_range_end.node_type)
builder.writeln('This paragraph is outside the editable range, and cannot be edited.')
doc.save(file_name=ARTIFACTS_DIR + 'EditableRange.CreateAndRemove.docx')
# Удалить редактируемый диапазон. Все узлы, находившиеся внутри диапазона, останутся нетронутыми.
editable_range.remove()
```

### See Also

* module [aspose.words](../../)
* class [EditableRangeStart](../)

