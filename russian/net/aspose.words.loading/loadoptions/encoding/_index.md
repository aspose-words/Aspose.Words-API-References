---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words для .NET
description: LoadOptions Encoding свойство. Получает или задает кодировку которая будет использоваться для загрузки документа HTML TXT или CHM если кодировка не указана внутри документа. Может бытьнулевой . По умолчаниюнулевой  на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Получает или задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть`нулевой` . По умолчанию`нулевой` .

```csharp
public Encoding Encoding { get; set; }
```

## Примечания

Это свойство используется только при загрузке документов HTML, TXT или CHM.

Если внутри документа не указана кодировка и это свойство`нулевой`то система попытается to автоматически определить кодировку.

## Примеры

Показывает, как установить кодировку для открытия документа.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Загрузите документ, передав объект LoadOptions, затем проверьте содержимое документа.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
