---
title: ImageFieldMergingArgs.image_file_name property
linktitle: image_file_name property
articleTitle: image_file_name property
second_title: Aspose.Words for Python
description: "ImageFieldMergingArgs.image_file_name property. Sets the file name of the image that the mail merge engine must insert into the document."
type: docs
weight: 10
url: /python-net/aspose.words.mailmerging/imagefieldmergingargs/image_file_name/
---

## ImageFieldMergingArgs.image_file_name property

Sets the file name of the image that the mail merge engine must insert into the document.


```python
@property
def image_file_name(self) -> str:
    ...

@image_file_name.setter
def image_file_name(self, value: str):
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

* module [aspose.words.mailmerging](../../)
* class [ImageFieldMergingArgs](../)

