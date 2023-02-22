---
title: FootnoteOptions.Columns
second_title: Aspose.Words لمراجع .NET API
description: FootnoteOptions ملكية. يحدد عدد الأعمدة التي يتم تنسيق منطقة الحواشي السفلية بها.
type: docs
weight: 10
url: /ar/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

يحدد عدد الأعمدة التي يتم تنسيق منطقة الحواشي السفلية بها.

```csharp
public int Columns { get; set; }
```

### ملاحظات

إذا كانت قيمة هذه الخاصية تساوي 0 ، فسيتم تنسيق منطقة الحواشي السفلية بعدد من الأعمدة بناءً على عدد الأعمدة في الصفحة المعروضة. القيمة الافتراضية هي 0.

### أمثلة

يوضح كيفية تقسيم قسم الحاشية السفلية إلى عدد معين من الأعمدة.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../footnoteoptions/)
* المجسم [Aspose.Words](../../../)


