---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection Color, чтобы легко настраивать и управлять цветами границ для ваших дизайнов. Улучшите свой пользовательский интерфейс с помощью ярких опций!
type: docs
weight: 20
url: /ru/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Получает или задает цвет границы.

```csharp
public Color Color { get; set; }
```

## Примечания

Возвращает цвет первой границы в коллекции.

Задает цвет всех границ в коллекции, за исключением диагональных границ.

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
