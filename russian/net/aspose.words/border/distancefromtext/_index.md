---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Border DistanceFromText, позволяющее легко настраивать расстояние от границ текста или краев страницы в пунктах для улучшенного управления макетом.
type: docs
weight: 20
url: /ru/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Возвращает или задает расстояние границы от текста или от края страницы в пунктах.

```csharp
public double DistanceFromText { get; set; }
```

## Примечания

Не имеет никакого эффекта и будет автоматически сброшен на ноль для границ ячеек таблицы.

## Примеры

Показывает, как создать широкую синюю полосу в верхней части первой страницы.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Смотрите также

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
