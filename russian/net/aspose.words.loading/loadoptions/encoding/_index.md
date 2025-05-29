---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LoadOptions Encoding для легкого управления кодировкой документов HTML TXT или CHM. Настройте загрузку контента для оптимальной производительности!
type: docs
weight: 50
url: /ru/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Возвращает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть`нулевой` . По умолчанию`нулевой` .

```csharp
public Encoding Encoding { get; set; }
```

## Примечания

Это свойство используется только при загрузке документов HTML, TXT или CHM.

Если кодировка не указана внутри документа и это свойство`нулевой`то система попытается автоматически определить кодировку to .

## Примеры

Показывает, как задать кодировку, в которой будет открываться документ.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Загружаем документ, передавая объект LoadOptions, затем проверяем содержимое документа.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
