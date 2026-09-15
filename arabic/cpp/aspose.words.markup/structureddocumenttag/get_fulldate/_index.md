---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_FullDate method"
linktitle: "get_FullDate"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_FullDate. تحدد التاريخ والوقت الكاملين اللذين تم إدخالهما آخر مرة في هذه الـ SDT في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_fulldate/
---
## StructuredDocumentTag::get_FullDate method


يحدد التاريخ والوقت الكاملين اللذين تم إدخالهما آخرًا في هذه **SDT**.

```cpp
System::DateTime Aspose::Words::Markup::StructuredDocumentTag::get_FullDate()
```

## ملاحظات


ستعمل الوصول إلى هذه الخاصية فقط مع نوع SDT [Date](../../sdttype/).

ستحدث استثناء لجميع أنواع SDT الأخرى.

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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
