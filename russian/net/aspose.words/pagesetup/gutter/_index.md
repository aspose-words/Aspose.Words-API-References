---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: Aspose.Words для .NET
description: Отрегулируйте настройки PageSetup Gutter, чтобы оптимизировать поля документа для переплета. Улучшите свой макет с помощью идеальных полей для профессиональных результатов.
type: docs
weight: 160
url: /ru/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Возвращает или задает размер дополнительного пространства, добавляемого к полю для переплета документа.

```csharp
public double Gutter { get; set; }
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

Показывает, как устанавливать поля переплета.

```csharp
Document doc = new Document();

// Вставьте текст, охватывающий несколько страниц.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Промежуток добавляет пробелы к левому или правому полю страницы,
// что компенсирует сгиб страниц в центре книги, нарушающий ее структуру.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Определите, сколько места отведено для текста на полях наших страниц, а затем добавьте величину для заполнения полей.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Установите свойство "RtlGutter" в значение "true", чтобы разместить переплет в более подходящем положении для текста, читаемого справа налево.
pageSetup.RtlGutter = true;

// Установите свойство "MultiplePages" на "MultiplePagesType.MirrorMargins" для чередования
// положение полей слева/справа на каждой странице.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
