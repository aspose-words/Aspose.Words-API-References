---
title: PageSetup.BorderSurroundsHeader
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Указывает включает ли граница страницы заголовок или исключает его.
type: docs
weight: 70
url: /ru/net/aspose.words/pagesetup/bordersurroundsheader/
---
## PageSetup.BorderSurroundsHeader property

Указывает, включает ли граница страницы заголовок или исключает его.

```csharp
public bool BorderSurroundsHeader { get; set; }
```

### Примечания

Обратите внимание: изменение этого свойства влияет на все разделы документа.

### Примеры

Показывает, как применить рамку к странице и верхнему/нижнему колонтитулу.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This is the main body text.");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer.");
builder.MoveToDocumentEnd();

// Вставляем синюю рамку в две линии.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.Borders.LineStyle = LineStyle.Double;
pageSetup.Borders.Color = Color.Blue;

// Объект PageSetup раздела имеет флаги «BorderSurroundsHeader» и «BorderSurroundsFooter», которые определяют
// окружает ли граница страницы основной текст, также включает верхний или нижний колонтитул соответственно.
// Установите для флага «BorderSurroundsHeader» значение «true», чтобы окружить заголовок нашей рамкой,
// а затем установите флаг «BorderSurroundsFooter», чтобы нижний колонтитул остался за пределами границы.
pageSetup.BorderSurroundsHeader = true;
pageSetup.BorderSurroundsFooter = false;

doc.Save(ArtifactsDir + "PageSetup.PageBorder.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


