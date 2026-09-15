---
title: "Aspose::Words::Markup::SdtDateStorageFormat enum"
linktitle: "SdtDateStorageFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::SdtDateStorageFormat enum. يحدد كيفية تخزين/استرجاع التاريخ لعنصر SDT من النوع تاريخ عندما يكون الـ SDT مرتبطًا بعقدة XML في مخزن بيانات المستند في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


يحدد كيفية تخزين/استرجاع التاريخ لعنصر SDT من نوع تاريخ عندما يكون الـ SDT مرتبطًا بعقدة XML في مخزن بيانات المستند.

```cpp
enum class SdtDateStorageFormat
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| التاريخ | 0 | يتم تخزين قيمة التاريخ لعنصر SDT من النوع تاريخ كقيمة تاريخ بصيغة تاريخ XML Schema القياسية. |
| DateTime | 1 | يتم تخزين قيمة التاريخ لعنصر SDT من النوع تاريخ كقيمة تاريخ بصيغة DateTime في XML Schema القياسية. |
| Text | 2 | يتم تخزين قيمة التاريخ لعنصر SDT من النوع تاريخ كنص. |
| Default | n/a | القيمة الافتراضية هي [DateTime](./) |


## أمثلة



يوضح كيفية مطالبة المستخدم بإدخال تاريخ باستخدام علامة مستند منسقة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أدرج علامة مستند منسقة تطلب من المستخدم إدخال تاريخ.
// في Microsoft Word، يُعرف هذا العنصر بـ "Date picker content control".
// عند النقر على السهم في الطرف الأيمن لهذه العلامة في Microsoft Word،
// سنرى نافذة منبثقة على شكل تقويم قابل للنقر.
// يمكننا استخدام تلك النافذة المنبثقة لتحديد تاريخ سيعرضه الوسم.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// اعرض التاريخ وفقًا لإعداد اللغة العربية السعودية.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// حدد الصيغة التي سيتم عرض التاريخ بها.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// اعرض التاريخ وفقًا للتقويم الهجري.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// قبل أن يختار المستخدم تاريخًا في Microsoft Word، سيعرض الوسم النص "Click here to enter a date.".
// وفقًا لتقويم الوسم، اضبط الخاصية "FullDate" لتجعل الوسم يعرض تاريخًا افتراضيًا.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
