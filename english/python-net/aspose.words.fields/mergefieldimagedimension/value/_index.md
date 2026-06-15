---
title: MergeFieldImageDimension.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for Python
description: "MergeFieldImageDimension.value property. The value."
type: docs
weight: 30
url: /python-net/aspose.words.fields/mergefieldimagedimension/value/
---

## MergeFieldImageDimension.value property

The value.


```python
@property
def value(self) -> float:
    ...

@value.setter
def value(self, value: float):
    ...

```

### Remarks

You should use a negative value to indicate that the original value of the corresponding image dimension
should be applied.


### Examples

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

### See Also

* module [aspose.words.fields](../../)
* class [MergeFieldImageDimension](../)

