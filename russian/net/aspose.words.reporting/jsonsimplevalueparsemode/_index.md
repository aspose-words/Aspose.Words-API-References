---
title: JsonSimpleValueParseMode Enum
linktitle: JsonSimpleValueParseMode
articleTitle: JsonSimpleValueParseMode
second_title: Aspose.Words для .NET
description: Aspose.Words.Reporting.JsonSimpleValueParseMode перечисление. Указывает режим анализа простых значений JSON нулевое логическое число целое число и строка при загрузке JSON. Такой режим не влияет на анализ значений даты и времени на С#.
type: docs
weight: 4700
url: /ru/net/aspose.words.reporting/jsonsimplevalueparsemode/
---
## JsonSimpleValueParseMode enumeration

Указывает режим анализа простых значений JSON (нулевое, логическое, число, целое число и строка) при загрузке JSON. Такой режим не влияет на анализ значений даты и времени.

```csharp
public enum JsonSimpleValueParseMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Loose | `0` | Указывает режим, в котором типы простых значений JSON определяются при анализе их строковых представлений. Например, тип «prop» из фрагмента JSON «{ prop: «123» }» в этом режиме определяется как целое число. |
| Strict | `1` | Указывает режим, в котором типы простых значений JSON определяются на основе самой нотации JSON. Например, тип 'prop' из фрагмента JSON '{ prop: "123" }' в этом режиме определяется как строка. |

### Смотрите также

* пространство имен [Aspose.Words.Reporting](../../aspose.words.reporting/)
* сборка [Aspose.Words](../../)
