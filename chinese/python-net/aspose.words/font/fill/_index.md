---
title: Font.fill property
linktitle: fill property
articleTitle: fill property
second_title: Aspose.Words for Python
description: "Font.fill property. Gets fill formatting for the [Font](../)."
type: docs
weight: 130
url: /zh/python-net/aspose.words/font/fill/
---

## Font.fill property

Gets fill formatting for the [Font](../).



```python
@property
def fill(self) -> aspose.words.drawing.Fill:
    ...

```

### Examples

Shows how to convert any of the fills back to solid fill.

```python
doc = aw.Document(file_name=MY_DIR + 'Two color gradient.docx')
# 获取第一个 Run 的 Font 的 Fill 对象。
fill = doc.first_section.body.paragraphs[0].runs[0].font.fill
# 检查 Font 的 Fill 属性。
print('The type of the fill is: {0}'.format(fill.fill_type))
print('The foreground color of the fill is: {0}'.format(fill.fore_color))
print('The fill is transparent at {0}%'.format(fill.transparency * 100))
# 将填充类型更改为具有统一绿色的实心。
fill.solid()
print('\nThe fill is changed:')
print('The type of the fill is: {0}'.format(fill.fill_type))
print('The foreground color of the fill is: {0}'.format(fill.fore_color))
print('The fill transparency is {0}%'.format(fill.transparency * 100))
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.FillSolid.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

