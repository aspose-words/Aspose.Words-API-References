---
title: Style.built_in property
linktitle: built_in property
articleTitle: built_in property
second_title: Aspose.Words for Python
description: "Style.built_in property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /zh/python-net/aspose.words/style/built_in/
---

## Style.built_in property

True if this style is one of the built-in styles in MS Word.


```python
@property
def built_in(self) -> bool:
    ...

```

### Examples

Shows how to differentiate custom styles from built-in styles.

```python
doc = aw.Document()
# 当我们使用 Microsoft Word 创建文档，或通过编程使用 Aspose.Words 时，
# 文档将附带一个样式集合，可用于应用于其文本以修改外观。
# 我们可以通过文档的 "Styles" 集合访问这些内置样式。
# 这些样式的 "BuiltIn" 标志都将设置为 "true"。
style = doc.styles.get_by_name('Emphasis')
self.assertTrue(style.built_in)
# 创建自定义样式并将其添加到集合中。
# 此类自定义样式的 "BuiltIn" 标志将设置为 "false"。
style = doc.styles.add(aw.StyleType.CHARACTER, 'MyStyle')
style.font.color = aspose.pydrawing.Color.navy
style.font.name = 'Courier New'
self.assertFalse(style.built_in)
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

