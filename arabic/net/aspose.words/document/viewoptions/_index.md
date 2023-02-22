---
title: Document.ViewOptions
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يوفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word .
type: docs
weight: 450
url: /ar/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

يوفر خيارات للتحكم في كيفية عرض المستند في Microsoft Word .

```csharp
public ViewOptions ViewOptions { get; }
```

### أمثلة

يوضح كيفية تعيين عامل تكبير مخصص ، أي الإصدارات القديمة من Microsoft Word سيتم تطبيقها على مستند عند التحميل.

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

يوضح كيفية تعيين نوع تكبير مخصص ، أي الإصدارات القديمة من Microsoft Word سيتم تطبيقها على مستند عند التحميل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بتعيين خاصية "ZoomType" على "ZoomType.PageWidth" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا ليلائم عرض الصفحة.
// قم بتعيين خاصية "ZoomType" على "ZoomType.FullPage" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا لجعل الصفحة الأولى بأكملها مرئية.
// قم بتعيين خاصية "ZoomType" على "ZoomType.TextFit" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا لملاءمة هوامش النص الداخلية للصفحة الأولى.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### أنظر أيضا

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


