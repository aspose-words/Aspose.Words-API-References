---
title: PageSetup.FooterDistance
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Возвращает или задает расстояние в пунктах между нижним колонтитулом и нижней частью страницы.
type: docs
weight: 140
url: /ru/net/aspose.words/pagesetup/footerdistance/
---
## PageSetup.FooterDistance property

Возвращает или задает расстояние (в пунктах) между нижним колонтитулом и нижней частью страницы.

```csharp
public double FooterDistance { get; set; }
```

### Примеры

Показывает, как настроить размер бумаги, ориентацию, поля, а также другие параметры раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


