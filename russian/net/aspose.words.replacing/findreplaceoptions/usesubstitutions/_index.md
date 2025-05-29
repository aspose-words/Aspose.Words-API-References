---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство UseSubstitutions в FindReplaceOptions. Легко включайте замены в шаблонах замены для повышения гибкости редактирования текста.
type: docs
weight: 190
url: /ru/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

Возвращает или задает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool UseSubstitutions { get; set; }
```

## Примечания

Подробную информацию об элементах подстановки см. по адресу: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

## Примеры

Показывает, как распознавать и использовать замены в шаблонах замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Использование устаревшего режима не поддерживает многие расширенные функции, поэтому нам нужно установить его в значение «false».
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

Показывает, как заменить текст с помощью подстановок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите свойство "UseSubstitutions" в значение "true", чтобы получить
// операция поиска и замены для распознавания элементов замены.
// Установите свойство «UseSubstitutions» в значение «false», чтобы игнорировать элементы подстановки.
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
