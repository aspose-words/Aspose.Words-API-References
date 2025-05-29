---
title: PageSetup.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "اتجاه إعداد الصفحة" لتعديل تخطيط صفحة مستندك بسهولة. حسّن طباعتك بإعدادات اتجاه قابلة للتخصيص!
type: docs
weight: 290
url: /ar/net/aspose.words/pagesetup/orientation/
---
## PageSetup.Orientation property

يعيد أو يضبط اتجاه الصفحة.

```csharp
public Orientation Orientation { get; set; }
```

## ملاحظات

تغيير`Orientation` المبادلات[`PageWidth`](../pagewidth/) و[`PageHeight`](../pageheight/).

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

يوضح كيفية تطبيق إعدادات إعداد الصفحة وإعادتها إلى الأقسام في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعديل خصائص إعداد الصفحة للقسم الحالي للمنشئ وإضافة نص.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// إذا بدأنا قسمًا جديدًا باستخدام منشئ المستندات،
// سوف يرث خصائص إعداد الصفحة الحالية للمنشئ.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// يمكننا إرجاع خصائص إعداد الصفحة إلى قيمها الافتراضية باستخدام طريقة "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### أنظر أيضا

* enum [Orientation](../../orientation/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
