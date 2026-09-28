---
title: Fill.color property
linktitle: color property
articleTitle: color property
second_title: Aspose.Words for Python
description: "Fill.color property. Gets or sets a Color object that represents the foreground color for the fill."
type: docs
weight: 50
url: /zh/python-net/aspose.words.drawing/fill/color/
---

## Fill.color property

Gets or sets a Color object that represents the foreground color for the fill.


```python
@property
def color(self) -> aspose.pydrawing.Color:
    ...

@color.setter
def color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This property preserves the alpha component of the aspose.pydrawing.Color,
unlike the [Fill.fore_color](../fore_color/) property, which resets it to fully opaque color.



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

* module [aspose.words.drawing](../../)
* class [Fill](../)

