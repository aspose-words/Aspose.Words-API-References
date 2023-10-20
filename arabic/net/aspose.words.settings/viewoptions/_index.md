---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Settings.ViewOptions فصل. يوفر خيارات متنوعة تتحكم في كيفية عرض المستند في برنامج Microsoft Word في C#.
type: docs
weight: 5950
url: /ar/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

يوفر خيارات متنوعة تتحكم في كيفية عرض المستند في برنامج Microsoft Word.

لمعرفة المزيد، قم بزيارة[العمل مع الخيارات ومظهر مستندات Word](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) مقالة توثيقية.

```csharp
public class ViewOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | إيقاف عرض المسافة بين أعلى النص والحافة العلوية للصفحة. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | يحدد ما إذا كانت الوثيقة في وضع تصميم النماذج. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | يتحكم في وضع العرض في Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | الحصول على أو تعيين النسبة المئوية (بين 10 و500) التي تريد عرض مستندك بها. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | الحصول على قيمة التكبير/التصغير أو تعيينها بناءً على حجم النافذة. |

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

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
