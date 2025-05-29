---
title: ViewOptions Class
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Settings.ViewOptions لتخصيص عرض المستندات في Microsoft Word، مما يعزز تجربة التحرير والإنتاجية لديك.
type: docs
weight: 6780
url: /ar/net/aspose.words.settings/viewoptions/
---
## ViewOptions class

يوفر خيارات مختلفة للتحكم في كيفية عرض المستند في Microsoft Word.

لمعرفة المزيد، قم بزيارة[العمل مع الخيارات ومظهر مستندات Word](https://docs.aspose.com/words/net/work-with-word-document-options-and-appearance/) مقالة توثيقية.

```csharp
public class ViewOptions
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayBackgroundShape](../../aspose.words.settings/viewoptions/displaybackgroundshape/) { get; set; } | يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة. |
| [DoNotDisplayPageBoundaries](../../aspose.words.settings/viewoptions/donotdisplaypageboundaries/) { get; set; } | يقوم بإيقاف عرض المسافة بين أعلى النص والحافة العلوية للصفحة. |
| [FormsDesign](../../aspose.words.settings/viewoptions/formsdesign/) { get; set; } | يحدد ما إذا كانت الوثيقة في وضع تصميم النماذج. |
| [ViewType](../../aspose.words.settings/viewoptions/viewtype/) { get; set; } | يتحكم في وضع العرض في Microsoft Word. |
| [ZoomPercent](../../aspose.words.settings/viewoptions/zoompercent/) { get; set; } | يحصل على النسبة المئوية التي تريد عرض مستندك بها أو يعينها. |
| [ZoomType](../../aspose.words.settings/viewoptions/zoomtype/) { get; set; } | يحصل على قيمة تكبير أو يعينها استنادًا إلى حجم النافذة. |

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

* class [Document](../../aspose.words/document/)
* property [ViewOptions](../../aspose.words/document/viewoptions/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
