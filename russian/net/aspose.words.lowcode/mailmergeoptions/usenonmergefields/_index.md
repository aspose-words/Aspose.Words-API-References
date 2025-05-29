---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words для .NET
description: Откройте расширенные возможности слияния почты с помощью свойства UseNonMergeFields. Бесшовная интеграция MERGEFIELD и других типов полей для расширенной настройки документов.
type: docs
weight: 130
url: /ru/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

Когда`истинный` , указывает, что в дополнение к полям MERGEFIELD слияние выполняется в некоторые другие типы полей и также в теги "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## Примечания

Обычно слияние почты выполняется только в поля MERGEFIELD, но несколько клиентов построили свои reporting с использованием других полей и создали много документов таким образом. Для упрощения миграции (и поскольку этот подход использовался независимо несколькими клиентами) была введена возможность слияния почты в другие поля.

Когда`UseNonMergeFields` установлен на`истинный`Aspose.Words выполнит слияние почты в следующие поля:

MERGEFIELD Имя поля

MACROBUTTON NOMACRO Имя поля

ЕСЛИ 0 = 0 "{ИмяПоля}" ""

Также, когда`UseNonMergeFields` установлен на`истинный`, Aspose.Words выполнит слияние почты в текст tags "{{fieldName}}". Это не поля, а просто текстовые теги.

### Смотрите также

* class [MailMergeOptions](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
