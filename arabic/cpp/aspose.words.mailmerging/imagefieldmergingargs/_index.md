---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::MailMerging::ImageFieldMergingArgs. توفر البيانات لحدث ImageFieldMerging(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


توفر البيانات لحدث [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/). لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | يعيد كائن [Document](../fieldmergingargsbase/get_document/) الذي يتم تنفيذ دمج البريد من أجله. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | يحصل على اسم حقل الدمج كما هو محدد في المستند. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | يحصل على الكائن الذي يمثل حقل الدمج الحالي. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | يحصل على اسم حقل الدمج في مصدر البيانات. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | يحصل على قيمة الحقل من مصدر البيانات. |
| [get_Image](./get_image/)() const | يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [get_ImageFileName](./get_imagefilename/)() const | يضبط اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [get_ImageHeight](./get_imageheight/)() const | يحدد ارتفاع الصورة لإدراجها في المستند. |
| [get_ImageStream](./get_imagestream/)() const | يحدد الدفق الذي يقرأ منه محرك دمج البريد الصورة. |
| [get_ImageWidth](./get_imagewidth/)() const | يحدد عرض الصورة لإدراجها في المستند. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | يحصل على الفهرس الصفري للسجل الذي يتم دمجه. |
| [get_Shape](./get_shape/)() const | يحدد الشكل الذي يجب على محرك دمج البريد إدراجه في المستند. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا كان الاسم غير متوفر. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | يضبط قيمة الحقل من مصدر البيانات. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | يحدد الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | يضبط اسم ملف الصورة التي يجب على محرك دمج البريد إدراجها في المستند. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | محدد القيمة لـ [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحدد الدفق الذي يقرأ منه محرك دمج البريد الصورة. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | محدد القيمة لـ [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | محدد القيمة لـ [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## ملاحظات


يحدث هذا الحدث أثناء دمج البريد عندما يتم العثور على حقل دمج بريد صورة في المستند. يمكنك الاستجابة لهذا الحدث لإرجاع اسم ملف أو دفق أو كائن **Image** إلى محرك دمج البريد بحيث يتم إدراجه في المستند.

هناك ثلاث خصائص متاحة [ImageFileName](./get_imagefilename/)، [ImageStream](./get_imagestream/) و[Image](./get_image/) لتحديد مصدر الصورة. اضبط واحدة فقط من هذه الخصائص.

لإدراج حقل دمج بريد صورة في مستند في Word، اختر أمر Insert/Field، ثم اختر MergeField واكتب Image:MyFieldName.

## انظر أيضًا

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
