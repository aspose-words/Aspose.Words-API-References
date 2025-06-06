---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection LineWidth, позволяющее легко настроить ширину границы в пунктах, повысив точность и визуальную привлекательность вашего дизайна.
type: docs
weight: 90
url: /ru/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Получает или задает ширину границы в пунктах.

```csharp
public double LineWidth { get; set; }
```

## Примечания

Возвращает ширину первой границы в коллекции.

Задает ширину всех границ в коллекции, за исключением диагональных границ.

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

* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
