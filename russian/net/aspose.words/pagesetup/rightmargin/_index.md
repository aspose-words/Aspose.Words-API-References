---
title: PageSetup.RightMargin
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Возвращает или задает расстояние в пунктах между правым краем страницы и правой границей основного текста.
type: docs
weight: 370
url: /ru/net/aspose.words/pagesetup/rightmargin/
---
## PageSetup.RightMargin property

Возвращает или задает расстояние (в пунктах) между правым краем страницы и правой границей основного текста.

```csharp
public double RightMargin { get; set; }
```

### Примеры

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
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


