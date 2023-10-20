---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words لـ .NET
description: BorderCollection LineStyle ملكية. الحصول على نمط الحدود أو تعيينه في C#.
type: docs
weight: 80
url: /ar/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

الحصول على نمط الحدود أو تعيينه.

```csharp
public LineStyle LineStyle { get; set; }
```

## ملاحظات

إرجاع نمط الحد الأول في المجموعة.

يضبط نمط كل الحدود في المجموعة باستثناء الحدود القطرية.

## أمثلة

يوضح كيفية إنشاء حدود صفحة خضراء متموجة مع الظل.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### أنظر أيضا

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
