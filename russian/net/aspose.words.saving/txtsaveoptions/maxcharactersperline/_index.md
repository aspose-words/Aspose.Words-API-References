---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words для .NET
description: TxtSaveOptions MaxCharactersPerLine свойство. Получает или задает целочисленное значение указывающее максимальное количество символов в одной строке. Значение по умолчанию  0 что означает отсутствие ограничений на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Получает или задает целочисленное значение, указывающее максимальное количество символов в одной строке. Значение по умолчанию — 0, что означает отсутствие ограничений.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Примеры

Показывает, как установить максимальное количество символов в строке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Установите максимально допустимую длину 30 символов в одной строке.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Смотрите также

* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
