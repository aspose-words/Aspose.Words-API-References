---
title: Document.cleanup method
linktitle: cleanup method
articleTitle: cleanup method
second_title: Aspose.Words for Python
description: "aspose.words.Document.cleanup method"
type: docs
weight: 590
url: /zh/python-net/aspose.words/document/cleanup/
---

## cleanup() {#default}

Cleans unused styles and lists from the document.


```python
def cleanup(self):
    ...
```

## cleanup(options) {#cleanupoptions}

Cleans unused styles and lists from the document depending on given [CleanupOptions](../../cleanupoptions/).



```python
def cleanup(self, options: aspose.words.CleanupOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | [CleanupOptions](../../cleanupoptions/) |  |

## Examples

Shows how to remove all unused custom styles from a document.

```python
doc = aw.Document()
doc.styles.add(aw.StyleType.LIST, 'MyListStyle1')
doc.styles.add(aw.StyleType.LIST, 'MyListStyle2')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle1')
doc.styles.add(aw.StyleType.CHARACTER, 'MyParagraphStyle2')
# 结合内置样式后，文档现在拥有八种样式。
# 只要文档中有任何文本，自定义样式就会被标记为 "已使用"。
# 使用该样式进行格式化。这意味着我们添加的 4 种样式目前未被使用。
self.assertEqual(8, doc.styles.count)
# 应用自定义字符样式，然后是自定义列表样式。这样会将它们标记为 "已使用"。
builder = aw.DocumentBuilder(doc=doc)
builder.font.style = doc.styles.get_by_name('MyParagraphStyle1')
builder.writeln('Hello world!')
doc_list = doc.lists.add(list_style=doc.styles.get_by_name('MyListStyle1'))
builder.list_format.list = doc_list
builder.writeln('Item 1')
builder.writeln('Item 2')
# 现在，有一个未使用的字符样式和一个未使用的列表样式。
# 当使用 CleanupOptions 对象配置时，Cleanup() 方法可以定位未使用的样式并将其移除。
cleanup_options = aw.CleanupOptions()
cleanup_options.unused_lists = True
cleanup_options.unused_styles = True
cleanup_options.unused_builtin_styles = True
doc.cleanup(cleanup_options)
self.assertEqual(4, doc.styles.count)
# 移除所有应用了自定义样式的节点会再次将其标记为 "未使用"。
# 重新运行 Cleanup 方法以将它们移除。
doc.first_section.body.remove_all_children()
doc.cleanup(cleanup_options)
self.assertEqual(2, doc.styles.count)
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

