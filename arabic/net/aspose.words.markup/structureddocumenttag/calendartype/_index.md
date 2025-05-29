---
title: StructuredDocumentTag.CalendarType
linktitle: CalendarType
articleTitle: CalendarType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTag CalendarType لتخصيص نوع تقويم SDT الخاص بك. حسّن مستنداتك بخيارات تقويم مخصصة!
type: docs
weight: 50
url: /ar/net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

يحدد نوع التقويم لهذا**SDT** . الافتراضي هوDefault

```csharp
public SdtCalendarType CalendarType { get; set; }
```

## ملاحظات

سيتم الوصول إلى هذه الخاصية فقط لـDate نوع SDT.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

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

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
