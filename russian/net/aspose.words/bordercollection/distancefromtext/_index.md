---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection DistanceFromText, чтобы легко настроить интервал между границами текста в ваших дизайнах. Оптимизируйте свой макет без усилий!
type: docs
weight: 40
url: /ru/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Возвращает или задает расстояние границы от текста в пунктах.

```csharp
public double DistanceFromText { get; set; }
```

## Примечания

Получает расстояние от текста до первой границы.

Устанавливает расстояние от текста для всех границ в коллекции, за исключением диагональных границ.

Не оказывает никакого эффекта и будет автоматически сброшено до нуля для границ ячеек таблицы.

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
