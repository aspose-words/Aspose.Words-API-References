---
title: ImageFieldMergingArgs.shape property
linktitle: shape property
articleTitle: shape property
second_title: Aspose.Words for Python
description: "ImageFieldMergingArgs.shape property. Specifies the shape that the mail merge engine must insert into the document."
type: docs
weight: 50
url: /python-net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---

## ImageFieldMergingArgs.shape property

Specifies the shape that the mail merge engine must insert into the document.


```python
@property
def shape(self) -> aspose.words.drawing.Shape:
    ...

@shape.setter
def shape(self, value: aspose.words.drawing.Shape):
    ...

```

### Remarks

When this property is specified, the mail merge engine ignores all other properties like [ImageFieldMergingArgs.image_file_name](../image_file_name/) or [ImageFieldMergingArgs.image_stream](../image_stream/)
and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field.
For example, you can specify [ShapeBase.wrap_type](../../../aspose.words.drawing/shapebase/wrap_type/) or any other shape property to fine tune the resulting node. However, please note that
you are responsible for providing the content of the shape.




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

