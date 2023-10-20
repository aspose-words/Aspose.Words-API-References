---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words لـ .NET
description: Fill ForeThemeColor ملكية. الحصول على أو تعيين كائن ThemeColor الذي يمثل اللون الأمامي للتعبئة في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

الحصول على أو تعيين كائن ThemeColor الذي يمثل اللون الأمامي للتعبئة.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## أمثلة

يوضح كيفية تعيين لون السمة للون شكل المقدمة/الخلفية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// ملاحظة: لا تستخدم "BackThemeColor" و"BackTintAndShade" لملء الخط.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### أنظر أيضا

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
