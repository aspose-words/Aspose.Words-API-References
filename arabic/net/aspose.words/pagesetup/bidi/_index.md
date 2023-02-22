---
title: PageSetup.Bidi
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. تحديد أن هذا القسم يحتوي على نص ثنائي الاتجاه نصوص معقدة.
type: docs
weight: 10
url: /ar/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

تحديد أن هذا القسم يحتوي على نص ثنائي الاتجاه (نصوص معقدة).

```csharp
public bool Bidi { get; set; }
```

### ملاحظات

عندما يكون صحيحًا ، يتم تخطيط الأعمدة في هذا القسم من اليمين إلى اليسار.

### أمثلة

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

// اضبط خاصية "Bidi" على "true" لترتيب الأعمدة بدءًا من الجانب الأيمن للصفحة.
// سيتطابق ترتيب الأعمدة مع اتجاه النص من اليمين إلى اليسار.
// اضبط خاصية "Bidi" على "false" لترتيب الأعمدة بدءًا من الجانب الأيسر للصفحة.
// سيتطابق ترتيب الأعمدة مع اتجاه النص من اليسار إلى اليمين.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


