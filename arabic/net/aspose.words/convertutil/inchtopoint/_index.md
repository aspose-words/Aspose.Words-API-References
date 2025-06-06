---
title: ConvertUtil.InchToPoint
linktitle: InchToPoint
articleTitle: InchToPoint
second_title: Aspose.Words لـ .NET
description: حوّل البوصات إلى نقاط بسهولة باستخدام طريقة InchToPoint من ConvertUtil. حسّن دقة تصميمك وقياساتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words/convertutil/inchtopoint/
---
## ConvertUtil.InchToPoint method

يحول البوصات إلى نقاط.

```csharp
public static double InchToPoint(double inches)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| inches | Double | القيمة المراد تحويلها. |

## ملاحظات

1 بوصة تساوي 72 نقطة.

## أمثلة

يوضح كيفية ضبط حجم الورق والاتجاه والهوامش، إلى جانب الإعدادات الأخرى لقسم ما.

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

يوضح كيفية تحديد خصائص الصفحة بالبوصات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يحدد "إعداد الصفحة" الخاص بالقسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام فئة "ConvertUtil" لاستخدام وحدة قياس أكثر شيوعًا،
// مثل البوصات عند تحديد الحدود.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

//البوصة تساوي 72 نقطة.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

//أضف محتوى لإظهار الهوامش الجديدة.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### أنظر أيضا

* class [ConvertUtil](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
