---
title: LayoutOptions.RevisionOptions
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words لـ .NET
description: استكشف خاصية LayoutOptions RevisionOptions للوصول بسهولة إلى إعدادات المراجعة وتخصيصها لتحسين التحكم في المستند والمرونة.
type: docs
weight: 70
url: /ar/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

يحصل على خيارات المراجعة.

```csharp
public RevisionOptions RevisionOptions { get; }
```

## أمثلة

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدرج مراجعة، ثم قم بتغيير لون جميع المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
