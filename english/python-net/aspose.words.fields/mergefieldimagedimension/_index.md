---
title: MergeFieldImageDimension class
linktitle: MergeFieldImageDimension class
articleTitle: MergeFieldImageDimension class
second_title: Aspose.Words for Python
description: "aspose.words.fields.MergeFieldImageDimension class. Represents an image dimension (i.e"
type: docs
weight: 1290
url: /python-net/aspose.words.fields/mergefieldimagedimension/
---

## MergeFieldImageDimension class

Represents an image dimension (i.e. the width or the height) used across a mail merge process.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

To indicate that the image should be inserted with its original dimension during a mail merge,
you should assign a negative value to the [MergeFieldImageDimension.value](./value/) property.



### Constructors
| Name | Description |
| --- | --- |
| [MergeFieldImageDimension(value)](./__init__/#float) | Creates an image dimension instance with the given value in points. |
| [MergeFieldImageDimension(value, unit)](./__init__/#float_mergefieldimagedimensionunit) | Creates an image dimension instance with the given value and the given unit. |

### Properties

| Name | Description |
| --- | --- |
| [unit](./unit/) | The unit. |
| [value](./value/) | The value. |

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
* enum [MergeFieldImageDimensionUnit](../mergefieldimagedimensionunit/)

