---
title: CompositeNode.insert_before method
linktitle: insert_before method
articleTitle: insert_before method
second_title: Aspose.Words for Python
description: "CompositeNode.insert_before method. Inserts the specified node immediately before the specified reference node."
type: docs
weight: 140
url: /ar/python-net/aspose.words/compositenode/insert_before/
---

## insert_before(new_child, ref_child) {#node_node}

Inserts the specified node immediately before the specified reference node.


```python
def insert_before(self, new_child: aspose.words.Node, ref_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The [Node](../../node/) to insert. |
| ref_child | [Node](../../node/) | The [Node](../../node/) that is the reference node. The *newChild* is placed before this node. |

### Remarks

If *refChild* is``None``, inserts *newChild* at the end of the list of child nodes.




If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The inserted node.


### Examples

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```python
doc = aw.Document()
# المستند الفارغ، بشكل افتراضي، يحتوي على فقرة واحدة.
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# العُقَد المركبة مثل فقرتنا يمكنها احتواء عُقَد مركبة أخرى وعُقَد داخلية كأطفال.
paragraph = doc.first_section.body.first_paragraph
paragraph_text = aw.Run(doc=doc, text='Initial text. ')
paragraph.append_child(paragraph_text)
# أنشئ ثلاث عقد تشغيل إضافية.
run1 = aw.Run(doc=doc, text='Run 1. ')
run2 = aw.Run(doc=doc, text='Run 2. ')
run3 = aw.Run(doc=doc, text='Run 3. ')
# لن يعرض جسم المستند هذه التشغيلات حتى ندرجها في عقدة مركبة
# التي هي نفسها جزء من شجرة عُقَد المستند، كما فعلنا مع التشغيل الأول.
# يمكننا تحديد مكان محتوى النص للعُقَد التي ندرجها
# يظهر في المستند عن طريق تحديد موقع الإدراج نسبة إلى عقدة أخرى في الفقرة.
self.assertEqual('Initial text.', paragraph.get_text().strip())
# أدرج التشغيل الثاني في الفقرة أمام التشغيل الأول.
paragraph.insert_before(run2, paragraph_text)
self.assertEqual('Run 2. Initial text.', paragraph.get_text().strip())
# أدرج التشغيل الثالث بعد التشغيل الأول.
paragraph.insert_after(run3, paragraph_text)
self.assertEqual('Run 2. Initial text. Run 3.', paragraph.get_text().strip())
# أدرج التشغيل الأول في بداية مجموعة عُقَد الأطفال للفقرة.
paragraph.prepend_child(run1)
self.assertEqual('Run 1. Run 2. Initial text. Run 3.', paragraph.get_text().strip())
self.assertEqual(4, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
# يمكننا تعديل محتوى التشغيل عن طريق تحرير وحذف عُقَد الأطفال الموجودة.
paragraph.get_child_nodes(aw.NodeType.RUN, True)[1].as_run().text = 'Updated run 2. '
paragraph.get_child_nodes(aw.NodeType.RUN, True).remove(paragraph_text)
self.assertEqual('Run 1. Updated run 2. Run 3.', paragraph.get_text().strip())
self.assertEqual(3, paragraph.get_child_nodes(aw.NodeType.ANY, True).count)
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

