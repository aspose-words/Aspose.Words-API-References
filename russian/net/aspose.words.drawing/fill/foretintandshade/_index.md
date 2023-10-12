---
title: Fill.ForeTintAndShade
second_title: Справочник по API Aspose.Words для .NET
description: Fill свойство. Получает или задает двойное значение которое осветляет или затемняет цвет переднего плана.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Получает или задает двойное значение, которое осветляет или затемняет цвет переднего плана.

```csharp
public double ForeTintAndShade { get; set; }
```

### Примечания

Допустимые значения для этого свойства находятся в диапазоне от -1 (самый темный) до 1 (самый светлый). Ноль (0) является нейтральным. Попытка установить для этого свойства значение меньше -1 или больше 1 приводит кArgumentOutOfRangeException.

### Примеры

Показывает, как управлять осветлением и затемнением цвета шрифта переднего плана.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Смотрите также

* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../fill/)
* сборка [Aspose.Words](../../../)


