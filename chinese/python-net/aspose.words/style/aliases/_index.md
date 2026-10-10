---
title: Style.aliases property
linktitle: aliases property
articleTitle: aliases property
second_title: Aspose.Words for Python
description: "Style.aliases property. Gets all aliases of this style"
type: docs
weight: 10
url: /zh/python-net/aspose.words/style/aliases/
---

## Style.aliases property

Gets all aliases of this style. If style has no aliases then empty array of string is returned.


```python
@property
def aliases(self) -> List[str]:
    ...

```

### Examples

Shows how to use style aliases.

```python
doc = aw.Document(file_name=MY_DIR + 'Style with alias.docx')
# 此文档包含一个名为 "MyStyle,MyStyle Alias 1,MyStyle Alias 2" 的样式。
# 如果样式的名称包含多个以逗号分隔的值，则每个子句都是一个单独的别名。
style = doc.styles.get_by_name('MyStyle')
self.assertEqual(['MyStyle Alias 1', 'MyStyle Alias 2'], list(style.aliases))
self.assertEqual('Title', style.base_style_name)
self.assertEqual('MyStyle Char', style.linked_style_name)
# 我们既可以使用别名，也可以使用名称来引用样式。
self.assertEqual(doc.styles.get_by_name('MyStyle Alias 1'), doc.styles.get_by_name('MyStyle Alias 2'))
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle Alias 1')
builder.writeln('Hello world!')
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle Alias 2')
builder.write('Hello again!')
self.assertEqual(doc.first_section.body.paragraphs[0].paragraph_format.style, doc.first_section.body.paragraphs[1].paragraph_format.style)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

