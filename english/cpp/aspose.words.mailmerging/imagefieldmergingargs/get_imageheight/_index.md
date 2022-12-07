---
title: get_ImageHeight
second_title: Aspose.Words for C++ API Reference
description: Specifies the image height for the image to insert into the document.
type: docs
weight: 40
url: /cpp/aspose.words.mailmerging/imagefieldmergingargs/get_imageheight/
---
## ImageFieldMergingArgs::get_ImageHeight method


Specifies the image height for the image to insert into the document.

```cpp
const System::SharedPtr<Aspose::Words::Fields::MergeFieldImageDimension> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight() const
```

## Remarks


The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property.

To indicate that the original value of the image height should be applied, you should assign the **null** value to this property or set the [Value](../../../aspose.words.fields/mergefieldimagedimension/get_value/) property for the instance of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property, to a negative value.

## See Also

* Class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words](../../../)
