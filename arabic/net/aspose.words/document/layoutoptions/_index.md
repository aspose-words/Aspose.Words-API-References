---
title: Document.LayoutOptions
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يحصل على أ خيارات التخطيط كائن يمثل خيارات للتحكم في عملية التخطيط لهذا المستند .
type: docs
weight: 230
url: /ar/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

يحصل على أ **خيارات التخطيط** كائن يمثل خيارات للتحكم في عملية التخطيط لهذا المستند .

```csharp
public LayoutOptions LayoutOptions { get; }
```

### أمثلة

يوضح كيفية إخفاء النص في مستند الإخراج المعروض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أدخل نصًا مخفيًا ، ثم حدد ما إذا كنا نرغب في حذفه من المستند المقدم.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

يوضح كيفية إظهار علامات الفقرات في مستند الإخراج الذي تم تقديمه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أضف بعض الفقرات ، ثم قم بتمكين علامات الفقرات لإظهار نهايات الفقرات
// مع رمز بيلكرو (¶) عند تقديم المستند.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


