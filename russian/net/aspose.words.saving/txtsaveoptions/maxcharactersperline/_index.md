---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words для .NET
description: Откройте для себя TxtSaveOptions MaxCharactersPerLine, легко установите ограничения на количество символов в строке для лучшего форматирования текста. Значение по умолчанию — 0 для неограниченного количества символов.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Возвращает или задает целочисленное значение, которое указывает максимальное количество символов в одной строке. Значение по умолчанию — 0, что означает отсутствие ограничений.

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

// Установите максимально допустимое количество символов в одной строке — 30.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Смотрите также

* class [TxtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
