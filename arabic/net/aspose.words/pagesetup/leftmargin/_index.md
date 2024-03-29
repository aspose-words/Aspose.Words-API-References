---
title: PageSetup.LeftMargin
linktitle: LeftMargin
articleTitle: LeftMargin
second_title: Aspose.Words لـ .NET
description: PageSetup LeftMargin ملكية. إرجاع أو تعيين المسافة بالنقاط بين الحافة اليسرى للصفحة والحد الأيسر للنص الأساسي في C#.
type: docs
weight: 200
url: /ar/net/aspose.words/pagesetup/leftmargin/
---
## PageSetup.LeftMargin property

إرجاع أو تعيين المسافة (بالنقاط) بين الحافة اليسرى للصفحة والحد الأيسر للنص الأساسي.

```csharp
public double LeftMargin { get; set; }
```

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

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
