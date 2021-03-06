---
title: Shadow
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает значение указывающее есть ли у границы тень.
type: docs
weight: 110
url: /ru/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Получает или задает значение, указывающее, есть ли у границы тень.

```csharp
public bool Shadow { get; set; }
```

### Примечания

Получает значение от первой границы в коллекции.

Задает значение для всех границ в коллекции, кроме диагональных границ.

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

* class [BorderCollection](../../bordercollection)
* пространство имен [Aspose.Words](../../bordercollection)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
