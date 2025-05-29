---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BorderCollection Shadow, чтобы улучшить свои проекты. Легко управляйте тенями границ для современного, стильного вида ваших проектов!
type: docs
weight: 110
url: /ru/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Возвращает или задает значение, указывающее, имеет ли граница тень.

```csharp
public bool Shadow { get; set; }
```

## Примечания

Получает значение из первой границы в коллекции.

Задает значение для всех границ в коллекции, за исключением диагональных границ.

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
