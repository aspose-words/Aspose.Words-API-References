---
title: ConvertUtil Class
linktitle: ConvertUtil
articleTitle: ConvertUtil
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ConvertUtil فصل. يوفر وظائف مساعدة للتحويل بين وحدات القياس المختلفة في C#.
type: docs
weight: 360
url: /ar/net/aspose.words/convertutil/
---
## ConvertUtil class

يوفر وظائف مساعدة للتحويل بين وحدات القياس المختلفة.

لمعرفة المزيد، قم بزيارة[التحويل بين وحدات القياس](https://docs.aspose.com/words/net/convert-between-measurement-units/) مقالة توثيقية.

```csharp
public static class ConvertUtil
```

## طُرق

| اسم | وصف |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(*double*) | تحويل البوصات إلى نقاط. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(*double*) | تحويل المليمترات إلى نقاط. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(*double, double, double*) | تحويل وحدات البكسل من دقة إلى أخرى. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(*double*) | تحويل البكسل إلى نقاط بدقة 96 نقطة في البوصة. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(*double, double*) | تحويل وحدات البكسل إلى نقاط بدقة بكسل محددة. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(*double*) | تحويل النقاط إلى بوصات. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(*double*) | تحويل النقاط إلى بكسل بدقة 96 نقطة في البوصة. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(*double, double*) | تحويل النقاط إلى بكسلات بدقة البكسل المحددة. |

## أمثلة

يوضح كيفية ضبط حجم الورق واتجاهه والهوامش بالإضافة إلى الإعدادات الأخرى لقسم ما.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

يوضح كيفية تحديد خصائص الصفحة بالبوصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يحدد "إعداد الصفحة" الخاص بالقسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام فئة "ConvertUtil" لاستخدام وحدة قياس مألوفة أكثر،
// مثل البوصات عند تحديد الحدود.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// البوصة تساوي 72 نقطة.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// أضف محتوى لتوضيح الهوامش الجديدة.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
