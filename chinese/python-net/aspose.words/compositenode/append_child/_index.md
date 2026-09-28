---
title: CompositeNode.append_child method
linktitle: append_child method
articleTitle: append_child method
second_title: Aspose.Words for Python
description: "CompositeNode.append_child method. Adds the specified node to the end of the list of child nodes for this node."
type: docs
weight: 80
url: /zh/python-net/aspose.words/compositenode/append_child/
---

## append_child(new_child) {#node}

Adds the specified node to the end of the list of child nodes for this node.


```python
def append_child(self, new_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


### Examples

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# 空白文档包含一个节、一个正文和一个段落。
# 调用 "RemoveAllChildren" 方法以移除所有这些节点，
# 并得到一个没有子节点的文档节点。
doc.remove_all_children()
# 此文档现在没有可添加内容的复合子节点。
# 如果我们想编辑它，需要重新填充其节点集合。
# 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
section = aw.Section(doc)
doc.append_child(section)
# 为该节设置一些页面布局属性。
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# 节需要一个正文，用于包含并显示其所有内容
# 在页面上位于节的页眉和页脚之间。
body = aw.Body(doc)
section.append_child(body)
# 创建一个段落，设置一些格式属性，然后将其作为子节点追加到正文。
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# 最后，添加一些内容以完成文档。创建一个 run，
# 设置其外观和内容，然后将其作为子节点追加到段落。
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

