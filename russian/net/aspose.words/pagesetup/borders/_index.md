---
title: PageSetup.Borders
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Получает коллекцию границ страницы.
type: docs
weight: 50
url: /ru/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Получает коллекцию границ страницы.

```csharp
public BorderCollection Borders { get; }
```

### Примеры

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


