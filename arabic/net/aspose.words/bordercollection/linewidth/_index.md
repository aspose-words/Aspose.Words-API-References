---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words لـ .NET
description: BorderCollection LineWidth ملكية. الحصول على أو تعيين عرض الحدود بالنقاط في C#.
type: docs
weight: 90
url: /ar/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

الحصول على أو تعيين عرض الحدود بالنقاط.

```csharp
public double LineWidth { get; set; }
```

## ملاحظات

إرجاع عرض الحد الأول في المجموعة.

يضبط عرض كافة الحدود في المجموعة باستثناء الحدود القطرية.

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

* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
