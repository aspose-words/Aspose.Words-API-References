---
title: PageSetup.RtlGutter
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Получает или задает использует ли Microsoft Word поля для раздела на основе языка с письмом справа налево или языка с письмом слева направо.
type: docs
weight: 380
url: /ru/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Получает или задает, использует ли Microsoft Word поля для раздела на основе языка с письмом справа налево или языка с письмом слева направо.

```csharp
public bool RtlGutter { get; set; }
```

### Примеры

Показывает, как установить поля переплета.

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

// Переплет добавляет пробелы либо к левому, либо к правому краю страницы,
// что компенсирует центральное сгибание страниц в книге, вторгающееся в макет страницы.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// Определите, сколько места на наших страницах отведено для текста внутри полей, а затем добавьте количество, чтобы заполнить поля.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Установите для свойства «RtlGutter» значение «true», чтобы разместить переплет в более подходящем положении для текста с письмом справа налево.
pageSetup.RtlGutter = true;

// Установите для свойства «MultiplePages» значение «MultiplePagesType.MirrorMargins», чтобы чередовать
// положение полей слева/справа на каждой странице.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


