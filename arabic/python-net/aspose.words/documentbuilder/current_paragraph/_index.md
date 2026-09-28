---
title: DocumentBuilder.current_paragraph property
linktitle: current_paragraph property
articleTitle: current_paragraph property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_paragraph property. Gets the paragraph that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 50
url: /ar/python-net/aspose.words/documentbuilder/current_paragraph/
---

## DocumentBuilder.current_paragraph property

Gets the paragraph that is currently selected in this [DocumentBuilder](../).



```python
@property
def current_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Remarks

[DocumentBuilder.current_node](../current_node/)



### Examples

Shows how to move a document builder's cursor to different nodes in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إنشاء إشارة مرجعية صالحة، كيان يتكون من عقد محاطة بعقدة بداية الإشارة المرجعية،
# وعقدة نهاية الإشارة المرجعية.
builder.start_bookmark('MyBookmark')
builder.write('Bookmark contents.')
builder.end_bookmark('MyBookmark')
first_paragraph_nodes = doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)
self.assertEqual(aw.NodeType.BOOKMARK_START, first_paragraph_nodes[0].node_type)
self.assertEqual(aw.NodeType.RUN, first_paragraph_nodes[1].node_type)
self.assertEqual('Bookmark contents.', first_paragraph_nodes[1].get_text().strip())
self.assertEqual(aw.NodeType.BOOKMARK_END, first_paragraph_nodes[2].node_type)
# المؤشر الخاص بمنشئ المستند يكون دائمًا أمام العقدة التي أضفناها آخر مرة باستخدامه.
# إذا كان مؤشر المنشئ في نهاية المستند، فستكون العقدة الحالية له فارغة (null).
# العقدة السابقة هي عقدة نهاية الإشارة المرجعية التي أضفناها آخر مرة.
# إضافة عقد جديدة باستخدام المنشئ سيُلحقها بالعقدة الأخيرة.
self.assertIsNone(builder.current_node)
# إذا أردنا تعديل جزء مختلف من المستند باستخدام المنشئ،
# سيتعين علينا نقل مؤشره إلى العقدة التي نرغب في تعديلها.
builder.move_to_bookmark(bookmark_name='MyBookmark')
# نقله إلى إشارة مرجعية سيجعل المؤشر ينتقل إلى أول عقدة داخل عقدتي بداية ونهاية الإشارة المرجعية، أي النص المغلق.
self.assertEqual(first_paragraph_nodes[1], builder.current_node)
# يمكننا أيضًا نقل المؤشر إلى عقدة فردية بهذه الطريقة.
builder.move_to(doc.first_section.body.first_paragraph.get_child_nodes(aw.NodeType.ANY, False)[0])
self.assertEqual(aw.NodeType.BOOKMARK_START, builder.current_node.node_type)
self.assertEqual(doc.first_section.body.first_paragraph, builder.current_paragraph)
self.assertTrue(builder.is_at_start_of_paragraph)
# يمكننا استخدام طرق محددة للانتقال إلى بداية/نهاية المستند.
builder.move_to_document_end()
self.assertTrue(builder.is_at_end_of_paragraph)
builder.move_to_document_start()
self.assertTrue(builder.is_at_start_of_paragraph)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

