---
title: Fill.transparency property
linktitle: transparency property
articleTitle: transparency property
second_title: Aspose.Words for Python
description: "Fill.transparency property. Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear)."
type: docs
weight: 200
url: /zh/python-net/aspose.words.drawing/fill/transparency/
---

## Fill.transparency property

Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear).


```python
@property
def transparency(self) -> float:
    ...

@transparency.setter
def transparency(self, value: float):
    ...

```

### Remarks

This property is the opposite of property [Fill.opacity](../opacity/).


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

