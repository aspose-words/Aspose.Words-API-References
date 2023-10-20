---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: PageSetup Bidi ملكية. يحدد أن هذا القسم يحتوي على نص ثنائي الاتجاه برامج نصية معقدة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

يحدد أن هذا القسم يحتوي على نص ثنائي الاتجاه (برامج نصية معقدة).

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

متى`حقيقي`، تم ترتيب الأعمدة الموجودة في هذا القسم من اليمين إلى اليسار.

## أمثلة

يوضح كيفية تعيين ترتيب أعمدة النص في القسم.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// اضبط الخاصية "Bidi" على "true" لترتيب الأعمدة بدءًا من الجانب الأيمن للصفحة.
// سيتطابق ترتيب الأعمدة مع اتجاه النص من اليمين إلى اليسار.
// اضبط الخاصية "Bidi" على "خطأ" لترتيب الأعمدة بدءًا من الجانب الأيسر للصفحة.
// سيتطابق ترتيب الأعمدة مع اتجاه النص من اليسار إلى اليمين.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
