---
title: RevisionOptions.ShowRevisionBars
linktitle: ShowRevisionBars
articleTitle: ShowRevisionBars
second_title: Aspose.Words لـ .NET
description: RevisionOptions ShowRevisionBars ملكية. يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من الأسطر التي تحتوي على محتوى تمت مراجعته. القيمة الافتراضية هيحقيقي  في C#.
type: docs
weight: 180
url: /ar/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من الأسطر التي تحتوي على محتوى تمت مراجعته. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ShowRevisionBars { get; set; }
```

## أمثلة

يوضح كيفية تغيير مظهر المراجعات في مستند الإخراج المقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مراجعة، ثم قم بتغيير لون كافة المراجعات إلى اللون الأخضر.
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

* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
