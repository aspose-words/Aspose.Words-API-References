---
title: Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth method
linktitle: get_ImageWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth method. Specifies the image width for the image to insert into the document in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.mailmerging/imagefieldmergingargs/get_imagewidth/
---
## ImageFieldMergingArgs::get_ImageWidth method


Specifies the image width for the image to insert into the document.

```cpp
const System::SharedPtr<Aspose::Words::Fields::MergeFieldImageDimension> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth() const
```

## Remarks


The value of this property initially comes from the corresponding MERGEFIELD's code, contained in the template document. To override the initial value, you should assign an instance of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class to this property or set the properties for the instance of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property.

To indicate that the original value of the image width should be applied, you should assign the **null** value to this property or set the [Value](../../../aspose.words.fields/mergefieldimagedimension/get_value/) property for the instance of [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/) class, returned by this property, to a negative value.

## See Also

* Class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
