---
title: PageSetup.BottomMargin
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. إرجاع أو تحديد المسافة بالنقاط بين الحافة السفلية للصفحة والحد السفلي للنص الأساسي.
type: docs
weight: 80
url: /ar/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

إرجاع أو تحديد المسافة (بالنقاط) بين الحافة السفلية للصفحة والحد السفلي للنص الأساسي.

```csharp
public double BottomMargin { get; set; }
```

### أمثلة

يوضح كيفية ضبط حجم الورق ، والاتجاه ، والهوامش ، إلى جانب الإعدادات الأخرى لقسم ما.

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
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


