---
title: RevisionOptions.InsertedTextColor
linktitle: InsertedTextColor
articleTitle: InsertedTextColor
second_title: Aspose.Words لـ .NET
description: خصّص تجربة التحرير لديك باستخدام خاصية InsertedTextColor في RevisionOptions، والتي تُحدّد ألوانًا فريدة للمحتوى المُدرج. افتراضيًا، ByAuthor.
type: docs
weight: 60
url: /ar/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

يسمح بتحديد اللون الذي سيتم استخدامه للمحتوى المدرجInsertion . القيمة الافتراضية هيByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
