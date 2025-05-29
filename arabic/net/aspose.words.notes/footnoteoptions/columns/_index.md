---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FootnoteOptions Columns لتنسيق الحواشي السفلية بسهولة باستخدام تخطيطات أعمدة قابلة للتخصيص لتحسين إمكانية القراءة والعرض.
type: docs
weight: 10
url: /ar/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

يحدد عدد الأعمدة التي سيتم تنسيق منطقة الحواشي السفلية بها.

```csharp
public int Columns { get; set; }
```

## ملاحظات

إذا كانت قيمة هذه الخاصية 0، فسيتم تنسيق منطقة الحواشي السفلية بعدد الأعمدة بناءً على عدد الأعمدة في الصفحة المعروضة. القيمة الافتراضية هي 0.

## أمثلة

يوضح كيفية تقسيم قسم الحاشية السفلية إلى عدد معين من الأعمدة.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
