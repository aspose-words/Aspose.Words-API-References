---
title: PageSetup.BottomMargin
linktitle: BottomMargin
articleTitle: BottomMargin
second_title: Aspose.Words для .NET
description: PageSetup BottomMargin свойство. Возвращает или задает расстояние в пунктах между нижним краем страницы и нижней границей основного текста на С#.
type: docs
weight: 80
url: /ru/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Возвращает или задает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста.

```csharp
public double BottomMargin { get; set; }
```

## Примеры

Показывает, как настроить размер бумаги, ориентацию, поля и другие параметры раздела.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
