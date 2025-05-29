---
title: RevisionOptions.ShowRevisionBars
linktitle: ShowRevisionBars
articleTitle: ShowRevisionBars
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ShowRevisionBars في RevisionOptions وضوح المستند من خلال عرض أشرطة المراجعة للمحتوى المُحرّر. افتراضيًا، صحيح.
type: docs
weight: 200
url: /ar/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

يسمح بتحديد ما إذا كان يجب عرض أشرطة المراجعة بالقرب من الأسطر التي تحتوي على محتوى منقح. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ShowRevisionBars { get; set; }
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

* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
