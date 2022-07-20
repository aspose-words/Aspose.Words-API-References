---
title: BottomMargin
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает или задает расстояние в пунктах между нижним краем страницы и нижней границей основного текста.
type: docs
weight: 80
url: /ru/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Возвращает или задает расстояние (в пунктах) между нижним краем страницы и нижней границей основного текста.

```csharp
public double BottomMargin { get; set; }
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

* class [PageSetup](../../pagesetup)
* пространство имен [Aspose.Words](../../pagesetup)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->