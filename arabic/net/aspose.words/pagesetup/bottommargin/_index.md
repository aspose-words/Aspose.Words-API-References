---
title: PageSetup.BottomMargin
linktitle: BottomMargin
articleTitle: BottomMargin
second_title: Aspose.Words لـ .NET
description: قم بضبط تخطيط مستندك باستخدام خاصية BottomMargin في PageSetup، مما يؤدي إلى تحديد المسافة بين الحافة السفلية للصفحة ونص الهيئة للحصول على عرض مثالي.
type: docs
weight: 80
url: /ar/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

يعيد أو يضبط المسافة (بالنقاط) بين الحافة السفلية للصفحة والحد السفلي لنص الجسم.

```csharp
public double BottomMargin { get; set; }
```

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

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
