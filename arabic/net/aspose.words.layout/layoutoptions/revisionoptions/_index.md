---
title: LayoutOptions.RevisionOptions
second_title: Aspose.Words لمراجع .NET API
description: LayoutOptions ملكية. يحصل على خيارات المراجعة .
type: docs
weight: 60
url: /ar/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

يحصل على خيارات المراجعة .

```csharp
public RevisionOptions RevisionOptions { get; }
```

### أمثلة

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج الذي تم تقديمه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مراجعة ، ثم قم بتغيير لون جميع المراجعات إلى اللون الأخضر.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// قم بإزالة الشريط الذي يظهر على يسار كل سطر تمت مراجعته.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### أنظر أيضا

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../layoutoptions/)
* المجسم [Aspose.Words](../../../)


