---
title: PageSetup.BorderDistanceFrom
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Получает или задает значение указывающее измеряется ли указанная граница страницы от края страницы или от текста который она окружает.
type: docs
weight: 40
url: /ru/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Получает или задает значение, указывающее, измеряется ли указанная граница страницы от края страницы или от текста, который она окружает.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

### Примеры

Показывает, как создать широкую синюю рамку в верхней части первой страницы.

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


