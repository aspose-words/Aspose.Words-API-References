---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PageSetup RtlGutter в Microsoft Word оптимизирует макеты разделов для языков с письмом справа налево и слева направо. Улучшите дизайн вашего документа!
type: docs
weight: 380
url: /ru/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Возвращает или задает, использует ли Microsoft Word отступы для раздела на основе языка с письмом справа налево или языка с письмом слева направо.

```csharp
public bool RtlGutter { get; set; }
```

## Примеры

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
