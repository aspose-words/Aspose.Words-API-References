---
title: Shading.ForegroundTintAndShade
second_title: Справочник по API Aspose.Words для .NET
description: Shading свойство. Получает или задает двойное значение которое осветляет или затемняет цвет темы переднего плана.
type: docs
weight: 60
url: /ru/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Получает или задает двойное значение, которое осветляет или затемняет цвет темы переднего плана.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) является нейтральным. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

Установка этого свойства для объекта Shading с цветами , не относящимися к теме, приводит кInvalidOperationException.

### Примеры

Показывает, как установить цвета переднего плана и фона для затенения текстуры.

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

* class [Shading](../)
* пространство имен [Aspose.Words](../../shading/)
* сборка [Aspose.Words](../../../)


