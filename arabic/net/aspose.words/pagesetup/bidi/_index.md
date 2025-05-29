---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup Bidi لتنسيق نص ثنائي الاتجاه بسلاسة. حسّن مستنداتك بدعم النصوص المعقدة لتحسين قابلية القراءة!
type: docs
weight: 10
url: /ar/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

يحدد أن هذا القسم يحتوي على نص ثنائي الاتجاه (نصوص معقدة).

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

متى`حقيقي`يتم ترتيب الأعمدة في هذا القسم من اليمين إلى اليسار.

## أمثلة

يوضح كيفية تعيين ترتيب أعمدة النص في قسم ما.

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

// قم بضبط الخاصية "Bidi" على "true" لترتيب الأعمدة بدءًا من الجانب الأيمن للصفحة.
//سيتوافق ترتيب الأعمدة مع اتجاه النص من اليمين إلى اليسار.
// قم بضبط خاصية "Bidi" على "false" لترتيب الأعمدة بدءًا من الجانب الأيسر للصفحة.
//سيتوافق ترتيب الأعمدة مع اتجاه النص من اليسار إلى اليمين.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
