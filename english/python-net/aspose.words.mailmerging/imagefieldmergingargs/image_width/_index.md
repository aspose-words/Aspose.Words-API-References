---
title: ImageFieldMergingArgs.image_width property
linktitle: image_width property
articleTitle: image_width property
second_title: Aspose.Words for Python
description: "ImageFieldMergingArgs.image_width property. Specifies the image width for the image to insert into the document."
type: docs
weight: 40
url: /python-net/aspose.words.mailmerging/imagefieldmergingargs/image_width/
---

## ImageFieldMergingArgs.image_width property

Specifies the image width for the image to insert into the document.


```python
@property
def image_width(self) -> aspose.words.fields.MergeFieldImageDimension:
    ...

@image_width.setter
def image_width(self, value: aspose.words.fields.MergeFieldImageDimension):
    ...

```

### Remarks

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the
template document. To override the initial value, you should assign an instance of
[MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class to this property or set the properties for the instance
of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property.


To indicate that the original value of the image width should be applied, you should assign the ``None``
value to this property or set the [MergeFieldImageDimension.value](../../../aspose.words.fields/mergefieldimagedimension/value/) property for the instance
of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property, to a negative value.





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

* module [aspose.words.mailmerging](../../)
* class [ImageFieldMergingArgs](../)
* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* enum [MergeFieldImageDimensionUnit](../../../aspose.words.fields/mergefieldimagedimensionunit/)

