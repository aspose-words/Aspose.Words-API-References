---
title: PageSetup.MultiplePages
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Для многостраничных документов получает или задает способ печати или отображения документа чтобы его можно было переплести как брошюру.
type: docs
weight: 260
url: /ru/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было переплести как брошюру.

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

### Примеры

Показывает, как настроить документ, который можно распечатать в виде книжки.

```csharp
Document doc = new Document();

// Вставить текст, занимающий 16 страниц.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Настройте свойство «PageSetup» первого раздела для печати документа в виде книжной складки.
// Когда мы печатаем этот документ с обеих сторон, мы можем взять страницы, чтобы сложить их
// и складываем их все сразу посередине. Содержимое документа выровняется в книжную складку.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Мы можем указать только количество листов, кратное 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Показывает, как установить поля желоба.

```csharp
Document doc = new Document();

// Вставляем текст, занимающий несколько страниц.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Желоб добавляет пробелы к левому или правому полю страницы,
// что компенсирует сгибание страниц по центру в книге, вторгающееся в макет страницы.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Определяем, сколько места на наших страницах есть для текста на полях, а затем добавляем количество для заполнения поля.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Установите для свойства "RtlGutter" значение "true", чтобы поместить поле в более подходящее положение для текста, написанного справа налево.
pageSetup.RtlGutter = true;

// Установите для свойства "MultiplePages" значение "MultiplePagesType.MirrorMargins" для чередования
// положение полей слева/справа на каждой странице.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Смотрите также

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


