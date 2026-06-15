---
title: MergeFieldImageDimension constructor
linktitle: MergeFieldImageDimension constructor
articleTitle: MergeFieldImageDimension constructor
second_title: Aspose.Words for Python
description: "aspose.words.fields.MergeFieldImageDimension constructor"
type: docs
weight: 10
url: /python-net/aspose.words.fields/mergefieldimagedimension/__init__/
---

## MergeFieldImageDimension(value) {#float}

Creates an image dimension instance with the given value in points.


```python
def __init__(self, value: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The value. |

### Remarks

You should use a negative value to indicate that the original value of the corresponding image dimension
should be applied.


## MergeFieldImageDimension(value, unit) {#float_mergefieldimagedimensionunit}

Creates an image dimension instance with the given value and the given unit.


```python
def __init__(self, value: float, unit: aspose.words.fields.MergeFieldImageDimensionUnit):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float | The value. |
| unit | [MergeFieldImageDimensionUnit](../../mergefieldimagedimensionunit/) | The unit. |

### Remarks

You should use a negative value to indicate that the original value of the corresponding image dimension
should be applied.


## Examples

Shows how to set the dimensions of images as MERGEFIELDS accepts them during a mail merge (MergedImageResizer).

```python
class MergedImageResizer(aw.mailmerging.IFieldMergingCallback):

    def __init__(self, image_width, image_height, unit):
        self.m_image_width = image_width
        self.m_image_height = image_height
        self.m_unit = unit

    def field_merging(self, e):
        raise Exception()

    def image_field_merging(self, args):
        args.image_file_name = str(args.field_value)
        args.image_width = aw.fields.MergeFieldImageDimension(value=self.m_image_width, unit=self.m_unit)
        args.image_height = aw.fields.MergeFieldImageDimension(value=self.m_image_height, unit=self.m_unit)
        self.assertEqual(self.m_image_width, args.image_width.value)
        self.assertEqual(self.m_unit, args.image_width.unit)
        self.assertEqual(self.m_image_height, args.image_height.value)
        self.assertEqual(self.m_unit, args.image_height.unit)
        self.assertIsNone(args.shape)
```

## See Also

* module [aspose.words.fields](../../)
* class [MergeFieldImageDimension](../)

