---
title: Fill.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words لـ .NET
description: خصّص تصميمك باستخدام خاصية BackThemeColor. عيّن بسهولة كائن ThemeColor لتحسين لون الخلفية وتحسين تجربة المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/fill/backthemecolor/
---
## Fill.BackThemeColor property

يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون الخلفية للتعبئة.

```csharp
public ThemeColor BackThemeColor { get; set; }
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
