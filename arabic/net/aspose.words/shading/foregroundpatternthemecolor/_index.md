---
title: Shading.ForegroundPatternThemeColor
second_title: Aspose.Words لمراجع .NET API
description: Shading ملكية. الحصول على أو تعيين لون سمة النمط الأمامي في نظام الألوان المطبق المرتبط بهذاShading الكائن.
type: docs
weight: 50
url: /ar/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

الحصول على أو تعيين لون سمة النمط الأمامي في نظام الألوان المطبق المرتبط بهذا[`Shading`](../) الكائن.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

### أمثلة

يوضح كيفية تعيين الألوان الأمامية والخلفية لتظليل الملمس.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### أنظر أيضا

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* مساحة الاسم [Aspose.Words](../../shading/)
* المجسم [Aspose.Words](../../../)


