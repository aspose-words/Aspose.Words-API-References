---
title: PageSetup.SheetsPerBooklet
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Возвращает или задает количество страниц которые будут включены в каждый буклет.
type: docs
weight: 400
url: /ru/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Возвращает или задает количество страниц, которые будут включены в каждый буклет.

```csharp
public int SheetsPerBooklet { get; set; }
```

### Примеры

Показывает, как настроить документ, который можно распечатать в виде сгиба книги.

```csharp
Document doc = new Document();

// Вставляем текст, занимающий 16 страниц.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Настройте свойство «PageSetup» первого раздела для печати документа в виде сгиба книги.
// Когда мы печатаем этот документ с обеих сторон, мы можем взять страницы и сложить их друг на друга
// и складываем их все сразу посередине. Содержимое документа выстроится в книжную складку.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Мы можем указать количество листов только кратное 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


