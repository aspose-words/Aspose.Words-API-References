---
title: ImageFieldMergingArgs.image_height property
linktitle: image_height property
articleTitle: image_height property
second_title: Aspose.Words for Python
description: "ImageFieldMergingArgs.image_height property. Specifies the image height for the image to insert into the document."
type: docs
weight: 20
url: /python-net/aspose.words.mailmerging/imagefieldmergingargs/image_height/
---

## ImageFieldMergingArgs.image_height property

Specifies the image height for the image to insert into the document.


```python
@property
def image_height(self) -> aspose.words.fields.MergeFieldImageDimension:
    ...

@image_height.setter
def image_height(self, value: aspose.words.fields.MergeFieldImageDimension):
    ...

```

### Remarks

The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the
template document. To override the initial value, you should assign an instance of
[MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class to this property or set the properties for the instance
of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property.


To indicate that the original value of the image height should be applied, you should assign the ``None``
value to this property or set the [MergeFieldImageDimension.value](../../../aspose.words.fields/mergefieldimagedimension/value/) property for the instance
of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property, to a negative value.





### See Also

* module [aspose.words.mailmerging](../../)
* class [ImageFieldMergingArgs](../)
* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* enum [MergeFieldImageDimensionUnit](../../../aspose.words.fields/mergefieldimagedimensionunit/)

