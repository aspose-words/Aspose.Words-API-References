---
title: FindReplaceOptions.LegacyMode
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. Получает или задает логическое значение указывающее что используется старый алгоритм поиска/замены.
type: docs
weight: 130
url: /ru/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Получает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены.

```csharp
public bool LegacyMode { get; set; }
```

### Примечания

Используйте этот флаг, если вам нужно точно такое же поведение, как и до введения расширенной функции поиска/замены. Обратите внимание, что старый алгоритм не поддерживает расширенные функции, такие как замена разрывами, применение форматирования и т. д.

### Примеры

Показывает, как распознавать и использовать замены в шаблонах замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// Использование устаревшего режима не поддерживает многие расширенные функции, поэтому нам нужно установить для него значение «false».
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


