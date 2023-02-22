---
title: FindReplaceOptions.FindWholeWordsOnly
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. True указывает что oldValue должно быть отдельным словом.
type: docs
weight: 50
url: /ru/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True указывает, что oldValue должно быть отдельным словом.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

### Примеры

Показывает, как переключать автономные операции поиска и замены только для слов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг "FindWholeWordsOnly" в "true", чтобы заменить найденный текст, если он не является частью другого слова.
// Установите флаг «FindWholeWordsOnly» в «false», чтобы заменить весь текст независимо от его окружения.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


