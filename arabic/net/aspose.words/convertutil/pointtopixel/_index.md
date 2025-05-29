---
title: ConvertUtil.PointToPixel
linktitle: PointToPixel
articleTitle: PointToPixel
second_title: Aspose.Words لـ .NET
description: حوّل النقاط إلى بكسلات بسهولة باستخدام طريقة PointToPixel من ConvertUtil، المُحسّنة بدقة 96 نقطة في البوصة. حسّن دقة تصميمك اليوم!
type: docs
weight: 60
url: /ar/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(*double*) {#pointtopixel}

يحول النقاط إلى بكسلات بدقة 96 نقطة في البوصة.

```csharp
public static double PointToPixel(double points)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| points | Double | القيمة المراد تحويلها. |

## ملاحظات

1 بوصة تساوي 72 نقطة.

## أمثلة

يوضح كيفية تحديد خصائص الصفحة بالبكسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يحدد "إعداد الصفحة" الخاص بالقسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام فئة "ConvertUtil" لاستخدام وحدة قياس مختلفة،
// مثل البكسلات عند تحديد الحدود.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// البكسل يساوي 0.75 نقطة.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// قيمة DPI الافتراضية المستخدمة هي 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

//أضف محتوى لإظهار الهوامش الجديدة.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### أنظر أيضا

* class [ConvertUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## PointToPixel(*double, double*) {#pointtopixel_1}

يحول النقاط إلى بكسلات بدقة البكسل المحددة.

```csharp
public static double PointToPixel(double points, double resolution)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| points | Double | القيمة المراد تحويلها. |
| resolution | Double | دقة dpi (نقطة لكل بوصة). |

## ملاحظات

1 بوصة تساوي 72 نقطة.

## أمثلة

يوضح كيفية استخدام تحويل النقاط إلى بكسلات بدقة افتراضية ومخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتحديد حجم الهامش العلوي لهذا القسم بالبكسل، وفقًا لـ DPI مخصص.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// عند قيمة DPI الافتراضية البالغة 96، يكون البكسل 0.75 نقطة.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// قم بتعيين DPI جديد واضبط قيمة الهامش العلوي وفقًا لذلك.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### أنظر أيضا

* class [ConvertUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
