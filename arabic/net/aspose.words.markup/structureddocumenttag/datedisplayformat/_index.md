---
title: StructuredDocumentTag.DateDisplayFormat
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. سلسلة تمثل التنسيق الذي يتم عرض التواريخ به. لا يمكن أن يكونباطل . التواريخ للغة الإنجليزية الولايات المتحدة هي mm/dd/yyyy
type: docs
weight: 90
url: /ar/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

سلسلة تمثل التنسيق الذي يتم عرض التواريخ به. لا يمكن أن يكون`باطل` . التواريخ للغة الإنجليزية (الولايات المتحدة) هي "mm/dd/yyyy"

```csharp
public string DateDisplayFormat { get; set; }
```

### ملاحظات

الوصول إلى هذه الخاصية سوف يعمل فقط من أجلDate نوع المعاملة الخاصة والتفضيلية.

بالنسبة لجميع أنواع SDT الأخرى، سيحدث استثناء.

### أمثلة

يوضح كيفية مطالبة المستخدم بإدخال تاريخ باستخدام علامة مستند منظمة.

```csharp
Document doc = new Document();

// أدخل علامة مستند منظمة تطالب المستخدم بإدخال تاريخ.
// في Microsoft Word، يُعرف هذا العنصر باسم "التحكم في محتوى منتقي التاريخ".
// عندما نضغط على السهم الموجود على الجانب الأيمن من هذه العلامة في Microsoft Word،
// سوف نرى نافذة منبثقة على شكل تقويم قابل للنقر عليه.
// يمكننا استخدام تلك النافذة المنبثقة لتحديد التاريخ الذي ستعرضه العلامة.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// عرض التاريخ حسب لغة المملكة العربية السعودية.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// قم بتعيين التنسيق الذي سيتم عرض التاريخ به.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// عرض التاريخ حسب التقويم الهجري.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// قبل أن يختار المستخدم تاريخًا في Microsoft Word، ستعرض العلامة النص "انقر هنا لإدخال التاريخ".
// وفقًا لتقويم العلامة، قم بتعيين خاصية "التاريخ الكامل" حتى تعرض العلامة تاريخًا افتراضيًا.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


