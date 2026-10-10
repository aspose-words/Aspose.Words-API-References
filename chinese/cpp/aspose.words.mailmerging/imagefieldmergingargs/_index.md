---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs 类"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs 类。提供 ImageFieldMerging() 事件的数据。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


为 [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/) 事件提供数据。要了解更多，请访问 [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) 文档文章。

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | 返回用于执行邮件合并的 [Document](../fieldmergingargsbase/get_document/) 对象。 |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | 获取文档中指定的合并字段名称。 |
| [get_Field](../fieldmergingargsbase/get_field/)() const | 获取表示当前合并字段的对象。 |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | 获取数据源中合并字段的名称。 |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | 获取来自数据源的字段值。 |
| [get_Image](./get_image/)() const | 指定邮件合并引擎必须插入到文档中的图像。 |
| [get_ImageFileName](./get_imagefilename/)() const | 设置邮件合并引擎必须插入到文档中的图像文件名。 |
| [get_ImageHeight](./get_imageheight/)() const | 指定要插入到文档中的图像高度。 |
| [get_ImageStream](./get_imagestream/)() const | 指定邮件合并引擎读取图像的流。 |
| [get_ImageWidth](./get_imagewidth/)() const | 指定要插入到文档中的图像宽度。 |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | 获取正在合并的记录的零基索引。 |
| [get_Shape](./get_shape/)() const | 指定邮件合并引擎必须插入到文档中的形状。 |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | 获取当前合并操作的数据表名称；如果名称不可用，则返回空字符串。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | 设置来自数据源的字段值。 |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | 指定邮件合并引擎必须插入到文档中的图像。 |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | 设置邮件合并引擎必须插入到文档中的图像文件名。 |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | 用于 [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/) 的 setter。 |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 指定邮件合并引擎读取图像的流。 |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | 用于 [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/) 的 setter。 |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | 用于 [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


当文档中遇到图像邮件合并字段时，此事件在邮件合并期间触发。您可以响应此事件以返回文件名、流或 **Image** 对象给邮件合并引擎，以便将其插入到文档中。

有三个属性可用 [ImageFileName](./get_imagefilename/)、[ImageStream](./get_imagestream/) 和 [Image](./get_image/)，用于指定图像的来源。仅设置这些属性中的一个。

要在 Word 文档中插入图像邮件合并字段，请选择 Insert/Field 命令，然后选择 MergeField 并键入 Image:MyFieldName。

## 另见

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
