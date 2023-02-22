---
title: BorderCollection.DistanceFromText
second_title: Справочник по API Aspose.Words для .NET
description: BorderCollection свойство. Получает или задает расстояние границы от текста в пунктах.
type: docs
weight: 40
url: /ru/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Получает или задает расстояние границы от текста в пунктах.

```csharp
public double DistanceFromText { get; set; }
```

### Примечания

Получает расстояние от текста для первой границы.

Задает расстояние от текста для всех границ в коллекции, кроме диагональных границ.

Не имеет никакого эффекта и будет автоматически обнулен для границ ячеек таблицы.

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


