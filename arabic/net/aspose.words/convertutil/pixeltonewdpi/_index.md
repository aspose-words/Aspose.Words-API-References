---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words لـ .NET
description: حوّل دقة البكسل بسهولة باستخدام طريقة PixelToNewDpi من ConvertUtil. حقق جودة ودقة صورة مثالية لمشاريعك.
type: docs
weight: 30
url: /ar/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

يحول وحدات البكسل من دقة إلى أخرى.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pixels | Double | القيمة المراد تحويلها. |
| oldDpi | Double | الدقة الحالية (نقطة لكل بوصة). |
| newDpi | Double | دقة dpi (نقطة لكل بوصة) الجديدة. |

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
