---
title: Aspose::Words::MailMerging::ImageFieldMergingArgs class
linktitle: ImageFieldMergingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::MailMerging::ImageFieldMergingArgs class. Provides data for the ImageFieldMerging() event. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Provides data for the [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/) event. To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) documentation article.

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Methods

| Method | Description |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Returns the [Document](../fieldmergingargsbase/get_document/) object for which the mail merge is performed. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Gets the name of the merge field as specified in the document. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Gets the object that represents the current merge field. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Gets the name of the merge field in the data source. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Gets the value of the field from the data source. |
| [get_Image](./get_image/)() const | Specifies the image that the mail merge engine must insert into the document. |
| [get_ImageFileName](./get_imagefilename/)() const | Sets the file name of the image that the mail merge engine must insert into the document. |
| [get_ImageHeight](./get_imageheight/)() const | Specifies the image height for the image to insert into the document. |
| [get_ImageStream](./get_imagestream/)() const | Specifies the stream for the mail merge engine to read an image from. |
| [get_ImageWidth](./get_imagewidth/)() const | Specifies the image width for the image to insert into the document. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Gets the zero based index of the record that is being merged. |
| [get_Shape](./get_shape/)() const | Specifies the shape that the mail merge engine must insert into the document. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Gets the name of the data table for the current merge operation or empty string if the name is not available. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Sets the value of the field from the data source. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Specifies the image that the mail merge engine must insert into the document. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Sets the file name of the image that the mail merge engine must insert into the document. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Setter for [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifies the stream for the mail merge engine to read an image from. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Setter for [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Setter for [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Remarks


This event occurs during mail merge when an image mail merge field is encountered in the document. You can respond to this event to return a file name, stream, or an **Image** object to the mail merge engine so it is inserted into the document.

There are three properties available [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) and [Image](./get_image/) to specify where the image must be taken from. Set only one of these properties.

To insert an image mail merge field into a document in Word, select Insert/Field command, then select MergeField and type Image:MyFieldName.

## See Also

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
