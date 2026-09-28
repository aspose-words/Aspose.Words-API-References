---
title: GeneralFormatCollection.remove_at method
linktitle: remove_at method
articleTitle: remove_at method
second_title: Aspose.Words for Python
description: "GeneralFormatCollection.remove_at method. Removes a general format occurrence at the specified index."
type: docs
weight: 50
url: /zh/python-net/aspose.words.fields/generalformatcollection/remove_at/
---

## remove_at(index) {#int}

Removes a general format occurrence at the specified index.


```python
def remove_at(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用文档生成器插入一个字段，以显示未应用任何格式的结果。
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# 我们可以使用字段的属性为字段的结果应用格式。
# 以下是我们可以应用于字段结果的三种格式类型。
# 1 - 数值格式：
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 - 日期/时间格式：
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 - 常规格式：
field = builder.insert_field(field_code='= 25 + 33')
format_obj = field.format
format_obj.general_formats.add(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.add(aw.fields.GeneralFormat.UPPER)
field.update()
index = 0
for general_format in format_obj.general_formats:
    print(f'General format index {index}: {general_format}')
    index += 1
self.assertEqual('= 25 + 33 \\* roman \\* Upper', field.get_field_code())
self.assertEqual('LVIII', field.result)
self.assertEqual(2, len(format_obj.general_formats))
self.assertEqual(aw.fields.GeneralFormat.LOWERCASE_ROMAN, format_obj.general_formats[0])
# 我们可以移除格式，使字段的结果恢复到原始形式。
format_obj.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.remove_at(0)
self.assertEqual(0, len(format_obj.general_formats))
field.update()
self.assertEqual('= 25 + 33  ', field.get_field_code())
self.assertEqual('58', field.result)
self.assertEqual(0, len(format_obj.general_formats))
```

### See Also

* module [aspose.words.fields](../../)
* class [GeneralFormatCollection](../)

