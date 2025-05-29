---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Document ViewOptions لتخصيص إعدادات عرض Microsoft Word للحصول على تجربة عرض مخصصة.
type: docs
weight: 490
url: /ar/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

يوفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
```

## أمثلة

يوضح كيفية تعيين عامل تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند تحميله.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

يوضح كيفية تعيين نوع تكبير مخصص، والذي ستطبقه الإصدارات القديمة من Microsoft Word على المستند عند تحميله.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// اضبط خاصية "ZoomType" على "ZoomType.PageWidth" للحصول على Microsoft Word
//لتكبير المستند تلقائيًا ليتناسب مع عرض الصفحة.
// اضبط خاصية "ZoomType" على "ZoomType.FullPage" للحصول على Microsoft Word
//لتكبير المستند تلقائيًا لجعل الصفحة الأولى بأكملها مرئية.
// اضبط خاصية "ZoomType" على "ZoomType.TextFit" للحصول على Microsoft Word
//لتكبير المستند تلقائيًا ليتناسب مع هوامش النص الداخلية للصفحة الأولى.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### أنظر أيضا

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
