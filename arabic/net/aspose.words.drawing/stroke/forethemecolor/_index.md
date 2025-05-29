---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words لـ .NET
description: أدر لون مقدمة خطك بسهولة باستخدام خاصية Stroke ForeThemeColor. خصّص تصاميمك بألوان زاهية!
type: docs
weight: 140
url: /ar/net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون المقدمة للحدود.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

## أمثلة

يوضح كيفية تعيين لون السمة والصبغة والظل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### أنظر أيضا

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
