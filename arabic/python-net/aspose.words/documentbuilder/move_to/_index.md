---
title: DocumentBuilder.move_to method
linktitle: move_to method
articleTitle: move_to method
second_title: Aspose.Words for Python
description: "DocumentBuilder.move_to method. Moves the cursor to an inline node or to the end of a paragraph."
type: docs
weight: 520
url: /ar/python-net/aspose.words/documentbuilder/move_to/
---

## move_to(node) {#node}

Moves the cursor to an inline node or to the end of a paragraph.


```python
def move_to(self, node: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../node/) | The node must be a paragraph or a direct child of a paragraph. |

### Remarks

When *node* is an inline-level node, the cursor is moved to this node
and further content will be inserted before that node.

When *node* is a [Paragraph](../../paragraph/), the cursor is moved to the end of the paragraph
and further content will be inserted just before the paragraph break.

When *node* is a block-level node but not a [Paragraph](../../paragraph/), the cursor is moved to the end of the first paragraph into block-level node
and further content will be inserted just before the paragraph break.




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

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# يمتلك مُنشئ المستند مؤشرًا، يعمل كجزء من المستند
# حيث يضيف المُنشئ عقدًا جديدة عندما نستخدم طرق بناء المستند الخاصة به.
# يعمل هذا المؤشر بنفس طريقة مؤشر وميض Microsoft Word،
# كما أنه دائمًا ما ينتهي مباشرةً بعد أي عقدة أضافها المُنشئ للتو.
# لإضافة محتوى إلى جزء مختلف من المستند،
# يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# المؤشر الآن أمام العقدة التي نقلناه إليها.
# إضافة سلسلة ثانية ستُدرجها أمام السلسلة الأولى.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# حرك المؤشر إلى نهاية المستند لمتابعة إلحاق النص بالنهاية كما كان من قبل.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

