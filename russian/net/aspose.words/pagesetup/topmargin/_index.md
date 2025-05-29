---
title: PageSetup.TopMargin
linktitle: TopMargin
articleTitle: TopMargin
second_title: Aspose.Words для .NET
description: Настройте свойство PageSetup TopMargin, чтобы задать расстояние от верхнего края страницы до текста, улучшив макет и удобочитаемость.
type: docs
weight: 440
url: /ru/net/aspose.words/pagesetup/topmargin/
---
## PageSetup.TopMargin property

Возвращает или задает расстояние (в пунктах) между верхним краем страницы и верхней границей основного текста.

```csharp
public double TopMargin { get; set; }
```

## Примеры

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
