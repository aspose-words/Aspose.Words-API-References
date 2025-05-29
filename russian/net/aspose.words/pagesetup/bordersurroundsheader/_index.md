---
title: PageSetup.BorderSurroundsHeader
linktitle: BorderSurroundsHeader
articleTitle: BorderSurroundsHeader
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup BorderSurroundsHeader для настройки границ страницы. Управляйте включением заголовка для создания безупречного макета документа.
type: docs
weight: 70
url: /ru/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Указывает, включает ли граница страницы заголовок или нет.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

## Примечания

Обратите внимание, что изменение этого свойства влияет на все разделы документа.

## Примеры

Показывает, как применить границу к странице и верхнему/нижнему колонтитулу.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Вставьте синюю двойную линию границы.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// Объект PageSetup раздела имеет флаги "BorderSurroundsHeader" и "BorderSurroundsFooter", которые определяют
// независимо от того, окружает ли рамка страницы основной текст, также включает верхний или нижний колонтитул соответственно.
// Установите флаг "BorderSurroundsHeader" в значение "true", чтобы окружить заголовок нашей рамкой,
// а затем установите флаг «BorderSurroundsFooter», чтобы оставить нижний колонтитул за пределами границы.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
