---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LastSection للوصول بسهولة إلى القسم الأخير من مستندك، مما يعزز كفاءة التنقل وإدارة المحتوى.
type: docs
weight: 250
url: /ar/net/aspose.words/document/lastsection/
---
## Document.LastSection property

يحصل على القسم الأخير في المستند.

```csharp
public Section LastSection { get; }
```

## ملاحظات

إرجاع`باطل`إذا لم تكن هناك أقسام.

## أمثلة

يوضح كيفية إنشاء قسم جديد باستخدام منشئ المستندات.

```csharp
Document doc = new Document();

// تحتوي الوثيقة الفارغة على قسم واحد بشكل افتراضي،
// والتي تحتوي على العقد الفرعية التي يمكننا تحريرها.
Assert.AreEqual(1, doc.Sections.Count);

//استخدم منشئ المستندات لإضافة نص إلى القسم الأول.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء قسم ثاني عن طريق إدراج فاصل قسم.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// كل قسم لديه إعدادات إعداد الصفحة الخاصة به.
//يمكننا تقسيم النص في القسم الثاني إلى عمودين.
// لن يؤثر هذا على النص الموجود في القسم الأول.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

### أنظر أيضا

* class [Section](../../section/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
