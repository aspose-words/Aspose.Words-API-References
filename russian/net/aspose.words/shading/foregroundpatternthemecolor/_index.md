---
title: Shading.ForegroundPatternThemeColor
linktitle: ForegroundPatternThemeColor
articleTitle: ForegroundPatternThemeColor
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство Shading ForegroundPatternThemeColor, чтобы улучшить цветовую схему вашего дизайна и повысить его визуальную привлекательность.
type: docs
weight: 50
url: /ru/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

Возвращает или задает цвет темы узора переднего плана в примененной цветовой схеме, которая связана с этим[`Shading`](../) объект.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

## Примеры

Показывает, как задать цвета переднего плана и фона для текстуры затенения.

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

### Смотрите также

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
