---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup SheetsPerBooklet, которое позволяет легко управлять количеством страниц в брошюре, улучшая макет документа и эффективность печати.
type: docs
weight: 400
url: /ru/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Возвращает или задает количество страниц, включаемых в каждую брошюру.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Примеры

Показывает, как настроить документ, который можно напечатать в виде книжного сгиба.

```csharp
Document doc = new Document();

// Вставьте текст, занимающий 16 страниц.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Настройте свойство «PageSetup» первого раздела для печати документа в виде книжного сгиба.
// Когда мы печатаем этот документ с обеих сторон, мы можем взять страницы и сложить их в стопку
// и сложите их все посередине одновременно. Содержимое документа выстроится в книжный сгиб.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Мы можем указать только количество листов, кратное 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
