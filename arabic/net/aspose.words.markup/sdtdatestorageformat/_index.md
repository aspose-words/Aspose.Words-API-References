---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.Markup.SdtDateStorageFormat على تحسين التعامل مع التاريخ في SDTs، مما يضمن تكامل بيانات XML بسلاسة في مستنداتك.
type: docs
weight: 4700
url: /ar/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

يحدد كيفية تخزين/استرجاع تاريخ SDT عندما يكون SDT مرتبطًا بعقدة XML في مخزن بيانات المستند.

```csharp
public enum SdtDateStorageFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Date | `0` | يتم تخزين قيمة التاريخ لتاريخ SDT كتاريخ بتنسيق XML Schema Date القياسي. |
| DateTime | `1` | يتم تخزين قيمة التاريخ لتاريخ SDT كتاريخ بتنسيق DateTime القياسي لمخطط XML. |
| Text | `2` | يتم تخزين قيمة التاريخ لتاريخ SDT كنص. |
| Default | `1` | الافتراضي هوDateTime |

## أمثلة

يوضح كيفية مطالبة المستخدم بإدخال تاريخ باستخدام علامة مستند منظمة.

```csharp
Document doc = new Document();

// أدخل علامة مستند منظمة تطلب من المستخدم إدخال تاريخ.
// في Microsoft Word، يُعرف هذا العنصر باسم "عنصر التحكم في محتوى اختيار التاريخ".
// عندما نضغط على السهم الموجود في الطرف الأيمن من هذه العلامة في Microsoft Word،
// سنرى نافذة منبثقة على شكل تقويم قابل للنقر.
//يمكننا استخدام تلك النافذة المنبثقة لتحديد التاريخ الذي سيعرضه العلامة.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

//عرض التاريخ حسب اللهجة العربية للمملكة العربية السعودية.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// تعيين التنسيق الذي سيتم عرض التاريخ به.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

//عرض التاريخ حسب التقويم الهجري.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// قبل أن يختار المستخدم تاريخًا في Microsoft Word، سيعرض العلامة النص "انقر هنا لإدخال تاريخ".
// وفقًا لتقويم العلامة، قم بتعيين خاصية "FullDate" لجعل العلامة تعرض تاريخًا افتراضيًا.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
