---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection LineStyle, чтобы настроить свой дизайн с помощью гибких стилей границ. Улучшите визуальную привлекательность вашего проекта без усилий!
type: docs
weight: 80
url: /ru/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Получает или задает стиль границы.

```csharp
public LineStyle LineStyle { get; set; }
```

## Примечания

Возвращает стиль первой границы в коллекции.

Задает стиль всех границ в коллекции, за исключением диагональных границ.

## Примеры

Показывает, как создать зеленую волнистую рамку страницы с тенью.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Смотрите также

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
