---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words для .NET
description: Настройте свойство Stroke ForeTintAndShade, чтобы легко осветлить или затемнить цвет переднего плана штриха для улучшения визуального эффекта.
type: docs
weight: 150
url: /ru/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Возвращает или задает двойное значение, которое осветляет или затемняет цвет переднего плана обводки.

```csharp
public double ForeTintAndShade { get; set; }
```

## Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) нейтрален. Попытка установить это свойство на значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

## Примеры

Показывает, как задать цвет, оттенок и тень темы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Смотрите также

* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
