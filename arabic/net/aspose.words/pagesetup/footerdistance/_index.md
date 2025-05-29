---
title: PageSetup.FooterDistance
linktitle: FooterDistance
articleTitle: FooterDistance
second_title: Aspose.Words لـ .NET
description: اضبط خاصية FooterDistance للتحكم في المسافة بين تذييل الصفحة وأسفلها. حسّن تصميم مستندك بسهولة!
type: docs
weight: 140
url: /ar/net/aspose.words/pagesetup/footerdistance/
---
## PageSetup.FooterDistance property

يعيد أو يضبط المسافة (بالنقاط) بين التذييل وأسفل الصفحة.

```csharp
public double FooterDistance { get; set; }
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
