---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::MailMerging::FieldMergingArgs. توفر البيانات لحدث MergeField. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


يوفر بيانات لحدث **MergeField**. لمعرفة المزيد، زر مقالة الوثائق [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | يعيد كائن [Document](../fieldmergingargsbase/get_document/) الذي يتم تنفيذ دمج البريد من أجله. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | يحصل على اسم حقل الدمج كما هو محدد في المستند. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | يحصل على الكائن الذي يمثل حقل الدمج الحالي. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | يحصل على اسم حقل الدمج في مصدر البيانات. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | يحصل على قيمة الحقل من مصدر البيانات. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | يحصل على الفهرس الصفري للسجل الذي يتم دمجه. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا كان الاسم غير متوفر. |
| [get_Text](./get_text/)() const | يحصل أو يضبط النص الذي سيتم إدراجه في المستند لحقل الدمج الحالي. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | يضبط قيمة الحقل من مصدر البيانات. |
| [set_Text](./set_text/)(const System::String\&) | المُعيّن لـ [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## ملاحظات


يحدث حدث **MergeField** أثناء دمج البريد عندما يتم العثور على حقل دمج بريد بسيط في المستند. يمكنك الاستجابة لهذا الحدث لإرجاع نص ليقوم محرك دمج البريد بإدراجه في المستند.

## انظر أيضًا

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
