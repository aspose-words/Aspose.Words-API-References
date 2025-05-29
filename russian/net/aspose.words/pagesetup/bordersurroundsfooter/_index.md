---
title: PageSetup.BorderSurroundsFooter
linktitle: BorderSurroundsFooter
articleTitle: BorderSurroundsFooter
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PageSetup BorderSurroundsFooter может улучшить макет документа, управляя включением нижнего колонтитула в границы страницы.
type: docs
weight: 60
url: /ru/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Указывает, включает ли граница страницы нижний колонтитул или нет.

```csharp
public bool BorderSurroundsFooter { get; set; }
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
