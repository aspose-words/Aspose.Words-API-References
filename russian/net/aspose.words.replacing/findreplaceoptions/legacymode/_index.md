---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FindReplaceOptions LegacyMode, позволяющее легко переключать классический алгоритм поиска/замены для улучшения функциональности и удобства работы пользователя.
type: docs
weight: 130
url: /ru/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Возвращает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены.

```csharp
public bool LegacyMode { get; set; }
```

## Примечания

Используйте этот флаг, если вам нужно точно такое же поведение, как и до появления расширенной функции поиска/замены. Обратите внимание, что старый алгоритм не поддерживает расширенные функции, такие как замена с разрывами, применение форматирования и т. д.

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

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
