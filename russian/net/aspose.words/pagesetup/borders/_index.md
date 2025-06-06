---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup Borders, чтобы легко получать доступ к границам страниц и настраивать их, придавая вашим документам изысканный и профессиональный вид.
type: docs
weight: 50
url: /ru/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Получает коллекцию границ страницы.

```csharp
public BorderCollection Borders { get; }
```

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
