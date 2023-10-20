---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words لـ .NET
description: ViewOptions ZoomType ملكية. الحصول على قيمة التكبير/التصغير أو تعيينها بناءً على حجم النافذة في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

الحصول على قيمة التكبير/التصغير أو تعيينها بناءً على حجم النافذة.

```csharp
public ZoomType ZoomType { get; set; }
```

## أمثلة

يوضح كيفية تعيين عامل تكبير مخصص، أي الإصدارات الأقدم من Microsoft Word سيتم تطبيقها على المستند عند التحميل.

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

يوضح كيفية تعيين نوع تكبير/تصغير مخصص، والإصدارات الأقدم من Microsoft Word التي سيتم تطبيقها على المستند عند التحميل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بتعيين خاصية "ZoomType" على "ZoomType.PageWidth" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا ليناسب عرض الصفحة.
// قم بتعيين خاصية "ZoomType" على "ZoomType.FullPage" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا لجعل الصفحة الأولى بأكملها مرئية.
// قم بتعيين خاصية "ZoomType" على "ZoomType.TextFit" للحصول على Microsoft Word
// لتكبير المستند تلقائيًا ليناسب هوامش النص الداخلي للصفحة الأولى.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### أنظر أيضا

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
