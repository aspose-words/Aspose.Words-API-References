---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LineWidth في BorderCollection لضبط عرض الحدود بالنقاط بسهولة، مما يعزز دقة تصميمك وجاذبيته البصرية.
type: docs
weight: 90
url: /ar/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

يحصل على عرض الحدود بالنقاط أو يعينه.

```csharp
public double LineWidth { get; set; }
```

## ملاحظات

إرجاع عرض الحد الأول في المجموعة.

تعيين عرض جميع الحدود في المجموعة باستثناء الحدود القطرية.

## أمثلة

يوضح كيفية إنشاء حدود صفحة متموجة باللون الأخضر مع ظل.

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

* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
