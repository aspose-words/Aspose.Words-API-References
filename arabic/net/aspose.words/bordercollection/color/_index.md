---
title: BorderCollection.Color
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection ملكية. الحصول على لون الحد أو تعيينه .
type: docs
weight: 20
url: /ar/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

الحصول على لون الحد أو تعيينه .

```csharp
public Color Color { get; set; }
```

### ملاحظات

إرجاع لون الحد الأول في المجموعة.

يضبط لون كل الحدود في المجموعة باستثناء الحدود القطرية.

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


