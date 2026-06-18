---
title: MergeFieldImageDimension.unit property
linktitle: unit property
articleTitle: unit property
second_title: Aspose.Words for Python
description: "MergeFieldImageDimension.unit property. The unit."
type: docs
weight: 20
url: /python-net/aspose.words.fields/mergefieldimagedimension/unit/
---

## MergeFieldImageDimension.unit property

The unit.


```python
@property
def unit(self) -> aspose.words.fields.MergeFieldImageDimensionUnit:
    ...

@unit.setter
def unit(self, value: aspose.words.fields.MergeFieldImageDimensionUnit):
    ...

```

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

