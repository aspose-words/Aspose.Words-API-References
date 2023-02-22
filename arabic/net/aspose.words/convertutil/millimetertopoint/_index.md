---
title: ConvertUtil.MillimeterToPoint
second_title: Aspose.Words لمراجع .NET API
description: ConvertUtil طريقة. تحويل المليمترات إلى نقاط .
type: docs
weight: 20
url: /ar/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

تحويل المليمترات إلى نقاط .

```csharp
public static double MillimeterToPoint(double millimeters)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| millimeters | Double | القيمة المطلوب تحويلها. |

### ملاحظات

1 بوصة تساوي 25.4 ملم. 1 بوصة تساوي 72 نقطة .

### أمثلة

يوضح كيفية تحديد خصائص الصفحة بالمليمترات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يحدد "إعداد الصفحة" في القسم حجم هوامش الصفحة بالنقاط.
// يمكننا أيضًا استخدام فئة "ConvertUtil" لاستخدام وحدة قياس أكثر شيوعًا ،
// مثل المليمترات عند تحديد الحدود.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// سم حوالي 28.3 نقطة.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// أضف محتوى لتوضيح الهوامش الجديدة.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### أنظر أيضا

* class [ConvertUtil](../)
* مساحة الاسم [Aspose.Words](../../convertutil/)
* المجسم [Aspose.Words](../../../)


