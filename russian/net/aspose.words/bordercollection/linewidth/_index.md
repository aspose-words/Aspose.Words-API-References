---
title: BorderCollection.LineWidth
second_title: Справочник по API Aspose.Words для .NET
description: BorderCollection свойство. Получает или задает ширину границы в пунктах.
type: docs
weight: 90
url: /ru/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Получает или задает ширину границы в пунктах.

```csharp
public double LineWidth { get; set; }
```

### Примечания

Возвращает ширину первой границы в коллекции.

Устанавливает ширину всех границ в коллекции, кроме диагональных границ.

### Примеры

Показывает, как создать зеленую волнистую границу страницы с тенью.

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
* пространство имен [Aspose.Words](../../bordercollection/)
* сборка [Aspose.Words](../../../)


