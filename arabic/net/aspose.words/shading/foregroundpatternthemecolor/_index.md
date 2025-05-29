---
title: Shading.ForegroundPatternThemeColor
linktitle: ForegroundPatternThemeColor
articleTitle: ForegroundPatternThemeColor
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تخصيص خاصية Shading ForegroundPatternThemeColor لتحسين مخطط الألوان في تصميمك ورفع جاذبيته البصرية.
type: docs
weight: 50
url: /ar/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

يحصل على لون سمة نمط المقدمة أو يعينه في مخطط الألوان المطبق المرتبط بهذا[`Shading`](../) الكائن.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

## أمثلة

يوضح كيفية تعيين ألوان المقدمة والخلفية لملمس التظليل.

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
