---
title: Shading.BackgroundPatternThemeColor
linktitle: BackgroundPatternThemeColor
articleTitle: BackgroundPatternThemeColor
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство Shading BackgroundPatternThemeColor, чтобы улучшить свой дизайн с помощью уникальных фоновых узоров и цветовых схем.
type: docs
weight: 20
url: /ru/net/aspose.words/shading/backgroundpatternthemecolor/
---
## Shading.BackgroundPatternThemeColor property

Возвращает или задает цвет темы фонового узора в примененной цветовой схеме, связанной с этим[`Shading`](../) объект.

```csharp
public ThemeColor BackgroundPatternThemeColor { get; set; }
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
