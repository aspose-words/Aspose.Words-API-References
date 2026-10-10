---
title: "Aspose::Words::Markup::SdtCalendarType enum"
linktitle: "SdtCalendarType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::SdtCalendarType enum. يحدد أنواع التقويمات الممكنة التي يمكن استخدامها لتحديد CalendarType في مستند Office Open XML بلغة C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


يحدد أنواع التقويمات الممكنة التي يمكن استخدامها لتحديد [CalendarType](../structureddocumenttag/get_calendartype/) في مستند Office Open XML.

```cpp
enum class SdtCalendarType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Default | 0 | يُستخدم كقيمة افتراضية في OOXML. يساوي [Gregorian](./). |
| Gregorian | n/a | يحدد أنه يجب استخدام التقويم الغريغوري كما هو معرف في ISO 8601. يجب تعريب هذا التقويم إلى اللغة المناسبة. |
| GregorianArabic | n/a | يحدد أنه يجب استخدام التقويم الغريغوري كما هو معرف في ISO 8601. يجب عرض قيم هذا التقويم باللغة العربية. |
| GregorianMeFrench | n/a | يحدد أنه يجب استخدام التقويم الغريغوري كما هو معرف في ISO 8600. يجب عرض قيم هذا التقويم بالفرنسية المستخدمة في الشرق الأوسط. |
| GregorianUs | n/a | يحدد أنه يجب استخدام التقويم الغريغوري كما هو معرف في ISO 8601. يجب عرض قيم هذا التقويم باللغة الإنجليزية. |
| GregorianXlitEnglish | n/a | يحدد أنه يجب استخدام التقويم الغريغوري كما هو معرف في ISO 8601. يجب أن تكون قيم هذا التقويم تمثيل السلاسل الإنجليزية بالحروف العربية المقابلة (الترجمة العربية للأحرف الإنجليزية للتقويم الغريغوري). |
| GregorianXlitFrench | n/a | يحدد أنه يجب استخدام التقويم الغريغوري كما هو معرف في ISO 8601. يجب أن تكون قيم هذا التقويم تمثيل السلاسل الفرنسية بالحروف العربية المقابلة (الترجمة العربية للأحرف الفرنسية للتقويم الغريغوري). |
| Hebrew | n/a | يحدد أنه يجب استخدام التقويم العبري القمري كما هو موضح في صيغة غاوس لعيد الفصح [CITATION] وإعادة الصياغة الكاملة للقانون الشفوي (مشناه توراه). |
| Hijri | n/a | يحدد أنه يجب استخدام التقويم الهجري القمري كما هو موضح من قبل المملكة العربية السعودية، وزارة الشؤون الإسلامية، الوقف، الدعوة والإرشاد. |
| اليابان | n/a | يحدد أنه يجب استخدام تقويم عهد الإمبراطور الياباني كما هو موضح في المعيار الصناعي الياباني JIS X 0301. |
| كوريا | n/a | يحدد أنه يجب استخدام تقويم العصر الكوري تانغون، كما هو موصوف في القانون الكوري رقم 4. |
| None | n/a | يحدد أنه لا يجب استخدام أي تقويم. |
| ساكا | n/a | يحدد أنه يجب استخدام تقويم عصر ساكا، كما هو موصوف من قبل لجنة إصلاح التقويم في الهند، كجزء من الفلك الهندي والمرشد البحري. |
| تايوان | n/a | يحدد أنه يجب استخدام التقويم التايواني، كما هو معرف في المعيار الوطني الصيني CNS 7648. |
| التايلاندية | n/a | يحدد أنه يجب استخدام التقويم التايلاندي، كما هو معرف في المرسوم الملكي للملك فاجيرافود (راما السادس) في الجريدة الملكية ب. هـ 2456 (1913 م) وبالمرسوم الصادر عن رئيس الوزراء فيبونسونغكرام (1941 م) لتبدأ السنة في الأول من يناير حسب التقويم الميلادي ولتعيين السنة الصفرية إلى السنة الميلادية 543 قبل الميلاد. |


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
