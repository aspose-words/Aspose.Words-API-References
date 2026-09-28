---
title: CleanupOptions class
linktitle: CleanupOptions class
articleTitle: CleanupOptions class
second_title: Aspose.Words for Python
description: "aspose.words.CleanupOptions class. Allows to specify options for document cleaning"
type: docs
weight: 160
url: /zh/python-net/aspose.words/cleanupoptions/
---

## CleanupOptions class

Allows to specify options for document cleaning.
To learn more, visit the [Clean Up a Document](https://docs.aspose.com/words/python-net/clean-up-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [CleanupOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [duplicate_style](./duplicate_style/) | Gets/sets a flag indicating whether duplicate styles should be removed from document. Default value is ``False``. |
| [unused_builtin_styles](./unused_builtin_styles/) | Specifies that unused [Style.built_in](../style/built_in/) styles should be removed from document. |
| [unused_lists](./unused_lists/) | Specifies whether unused list and list definitions should be removed from document. Default value is ``True``. |
| [unused_styles](./unused_styles/) | Specifies whether unused styles should be removed from document. Default value is ``True``. |

### Examples

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

### See Also

* module [aspose.words](../)

