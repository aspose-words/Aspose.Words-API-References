---
title: Document.LastSection
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. للحصول على القسم الأخير في المستند.
type: docs
weight: 240
url: /ar/net/aspose.words/document/lastsection/
---
## Document.LastSection property

للحصول على القسم الأخير في المستند.

```csharp
public Section LastSection { get; }
```

### ملاحظات

إرجاع`باطل` إذا لم تكن هناك أقسام.

### أمثلة

يوضح كيفية إنشاء قسم جديد باستخدام أداة إنشاء المستندات.

```csharp
Document doc = new Document();

// يحتوي المستند الفارغ على قسم واحد افتراضيًا،
// الذي يحتوي على العقد الفرعية التي يمكننا تحريرها.
Assert.AreEqual(1, doc.Sections.Count);

// استخدم منشئ المستندات لإضافة نص إلى القسم الأول.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// أنشئ قسمًا ثانيًا عن طريق إدراج فاصل مقطعي.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// لكل قسم إعدادات إعداد الصفحة الخاصة به.
// يمكننا تقسيم النص في القسم الثاني إلى عمودين.
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
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


