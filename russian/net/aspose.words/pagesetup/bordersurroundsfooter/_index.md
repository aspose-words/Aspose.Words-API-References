---
title: PageSetup.BorderSurroundsFooter
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Указывает включает ли граница страницы нижний колонтитул или исключает его.
type: docs
weight: 60
url: /ru/net/aspose.words/pagesetup/bordersurroundsfooter/
---
## PageSetup.BorderSurroundsFooter property

Указывает, включает ли граница страницы нижний колонтитул или исключает его.

```csharp
public bool BorderSurroundsFooter { get; set; }
```

### Примечания

Обратите внимание: изменение этого свойства влияет на все разделы документа.

### Примеры

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

// Вставляем синюю двойную границу.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// Объект PageSetup раздела имеет флаги "BorderSurroundsHeader" и "BorderSurroundsFooter", которые определяют
// независимо от того, окружает ли граница страницы основной основной текст, также включает верхний или нижний колонтитул соответственно.
// Установите для флага "BorderSurroundsHeader" значение "true", чтобы окружить заголовок нашей рамкой,
// а затем установите флаг «BorderSurroundsFooter», чтобы оставить нижний колонтитул за границей.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


