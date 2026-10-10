---
title: "Aspose::Words::MailMerging::MailMerge::Execute method"
linktitle: "تنفيذ"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::MailMerging::MailMerge::Execute method. تُجري عملية دمج بريد لسجل واحد في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


يُجري عملية دمج بريد لسجل واحد.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | مصفوفة من أسماء حقول الدمج. أسماء الحقول غير حساسة لحالة الأحرف. إذا تم العثور على اسم حقل غير موجود في المستند، يتم تجاهله. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | مصفوفة من القيم التي سيتم إدراجها في حقول الدمج. يجب أن يكون عدد العناصر في هذه المصفوفة مساويًا لعدد العناصر في *fieldNames*. |
## ملاحظات


استخدم هذه الطريقة لملء حقول دمج البريد في المستند بالقيم من مصفوفة من الكائنات.

تقوم هذه الطريقة بدمج البيانات لسجل واحد فقط. تمثل مصفوفة أسماء الحقول ومصفوفة القيم بيانات سجل واحد.

هذه الطريقة لا تستخدم مناطق دمج البريد.

تتجاهل هذه الطريقة خيار [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## أمثلة



يظهر كيفية دمج صورة من URI كبيانات دمج بريد في MERGEFIELD.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// ستستقبل MERGEFIELDs ذات العلامات \"Image:\" صورة أثناء دمج البريد.
// السلسلة بعد النقطتين في العلامة \"Image:\" تتطابق مع اسم عمود
// في مصدر البيانات الذي تحتوي خلاياه على عناوين URI لملفات الصور.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// أنشئ مصدر بيانات يحتوي على عناوين URI للصور التي سنقوم بدمجها.
// يمكن أن يكون URI عنوان URL ويب يشير إلى صورة، أو اسم ملف محلي على نظام الملفات لصورة.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// نفّذ دمج بريد على مصدر بيانات يحتوي على صف واحد.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## انظر أيضًا

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


يُجري دمج بريد من مصدر بيانات مخصص.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | كائن ينفّذ واجهة مصدر بيانات دمج البريد المخصصة. |
## ملاحظات


استخدم هذه الطريقة لملء حقول دمج البريد في المستند بالقيم من أي مصدر بيانات مثل قائمة أو جدول تجزئة أو كائنات. تحتاج إلى كتابة فئة خاصة بك تنفّذ واجهة [IMailMergeDataSource](../../imailmergedatasource/).

يمكنك استخدام هذه الطريقة فقط عندما تكون [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false**، أي أنك لا تحتاج إلى توافق مع اللغات من اليمين إلى اليسار (مثل العربية أو العبرية).

تتجاهل هذه الطريقة خيار [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## انظر أيضًا

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
