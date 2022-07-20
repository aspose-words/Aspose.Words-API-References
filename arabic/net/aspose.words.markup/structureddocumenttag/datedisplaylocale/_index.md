---
title: DateDisplayLocale
second_title: Aspose.Words لمراجع .NET API
description: يسمح بتعيين / الحصول على تنسيق اللغة للتاريخ المعروض في هذا المعاملة الخاصة والتفضيلية .
type: docs
weight: 100
url: /ar/net/aspose.words.markup/structureddocumenttag/datedisplaylocale/
---
## StructuredDocumentTag.DateDisplayLocale property

يسمح بتعيين / الحصول على تنسيق اللغة للتاريخ المعروض في هذا **المعاملة الخاصة والتفضيلية** .

```csharp
public int DateDisplayLocale { get; set; }
```

### ملاحظات

الوصول إلى هذه الخاصية سيعمل فقط من أجلDate نوع SDT .

سيحدث استثناء لجميع أنواع المعاملة الخاصة والتفضيلية الأخرى.

### أمثلة

يوضح كيفية مطالبة المستخدم بإدخال تاريخ بعلامة مستند منظم.

```csharp
Document doc = new Document();

// أدخل علامة مستند منظم تطالب المستخدم بإدخال تاريخ.
// في Microsoft Word ، يُعرف هذا العنصر باسم "عنصر تحكم محتوى منتقي التاريخ".
// عندما نضغط على السهم الموجود في الطرف الأيمن من هذه العلامة في Microsoft Word ،
// سنرى نافذة منبثقة في شكل تقويم قابل للنقر.
// يمكننا استخدام تلك النافذة المنبثقة لتحديد التاريخ الذي ستعرضه العلامة.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// عرض التاريخ حسب اللغة العربية السعودية.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// اضبط التنسيق الذي تريد عرض التاريخ به.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// عرض التاريخ حسب التقويم الهجري.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// قبل أن يختار المستخدم تاريخًا في Microsoft Word ، ستعرض العلامة النص "انقر هنا لإدخال تاريخ.".
// وفقًا لتقويم العلامة ، قم بتعيين الخاصية "FullDate" للحصول على العلامة لعرض التاريخ الافتراضي.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../../structureddocumenttag)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->