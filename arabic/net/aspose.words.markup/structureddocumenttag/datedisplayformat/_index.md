---
title: StructuredDocumentTag.DateDisplayFormat
linktitle: DateDisplayFormat
articleTitle: DateDisplayFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StructuredDocumentTag DateDisplayFormat لتخصيص تنسيقات عرض التاريخ بسهولة. حسّن وضوح مستندك وجاذبيته!
type: docs
weight: 90
url: /ar/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

سلسلة تمثل التنسيق الذي يتم به عرض التواريخ.

```csharp
public string DateDisplayFormat { get; set; }
```

## ملاحظات

لا يمكن أن يكون`باطل`.

التواريخ للغة الإنجليزية (الولايات المتحدة) هي "mm/dd/yyyy"

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

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
