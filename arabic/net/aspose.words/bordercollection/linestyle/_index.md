---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BorderCollection LineStyle لتخصيص تصميمك بأنماط حدود مرنة. حسّن مظهر مشروعك البصري بسهولة!
type: docs
weight: 80
url: /ar/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

يحصل على نمط الحدود أو يعينه.

```csharp
public LineStyle LineStyle { get; set; }
```

## ملاحظات

إرجاع نمط الحدود الأولى في المجموعة.

تعيين نمط جميع الحدود في المجموعة باستثناء الحدود القطرية.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
