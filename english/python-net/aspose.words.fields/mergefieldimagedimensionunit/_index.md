---
title: MergeFieldImageDimensionUnit enumeration
linktitle: MergeFieldImageDimensionUnit enumeration
articleTitle: MergeFieldImageDimensionUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.fields.MergeFieldImageDimensionUnit enumeration. Specifies an unit of an image dimension (i.e"
type: docs
weight: 1300
url: /python-net/aspose.words.fields/mergefieldimagedimensionunit/
---

## MergeFieldImageDimensionUnit enumeration

Specifies an unit of an image dimension (i.e. the width or the height) used across a mail merge process.


### Members

| Name | Description |
| --- | --- |
| POINT | The point (i.e. 1/72 inch). |
| PERCENT | The percent of the original image dimension value. |

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

* module [aspose.words.fields](../)

