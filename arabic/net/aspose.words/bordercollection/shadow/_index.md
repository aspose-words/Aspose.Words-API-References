---
title: BorderCollection.Shadow
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الحدود لها ظل .
type: docs
weight: 110
url: /ar/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

الحصول على أو تعيين قيمة تشير إلى ما إذا كانت الحدود لها ظل .

```csharp
public bool Shadow { get; set; }
```

### ملاحظات

الحصول على القيمة من الحد الأول في المجموعة.

يضبط قيمة كل الحدود في المجموعة باستثناء الحدود القطرية.

### أمثلة

يوضح كيفية إنشاء حد صفحة أخضر مموج بظل.

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
* مساحة الاسم [Aspose.Words](../../bordercollection/)
* المجسم [Aspose.Words](../../../)


