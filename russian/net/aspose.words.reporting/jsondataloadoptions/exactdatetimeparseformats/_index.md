---
title: JsonDataLoadOptions.ExactDateTimeParseFormats
linktitle: ExactDateTimeParseFormats
articleTitle: ExactDateTimeParseFormats
second_title: Aspose.Words для .NET
description: JsonDataLoadOptions ExactDateTimeParseFormats свойство. Получает или задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. Значение по умолчаниюнулевой  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.reporting/jsondataloadoptions/exactdatetimeparseformats/
---
## JsonDataLoadOptions.ExactDateTimeParseFormats property

Получает или задает точные форматы для анализа значений даты и времени JSON при загрузке JSON. Значение по умолчанию:`нулевой` .

```csharp
public IEnumerable<string> ExactDateTimeParseFormats { get; set; }
```

## Примечания

Строки, закодированные с использованием формата даты и времени Microsoft® JSON (например, «/Date(1224043200000)/»), всегда распознаются как значения даты и времени независимо от значения этого свойства. Свойство определяет дополнительные форматы , которые будут использоваться при анализе значений даты и времени из строк следующим образом:

* Когда`ExactDateTimeParseFormats` является`нулевой` формат ISO-8601 и все форматы даты и времени , поддерживаемые для текущей культуры, английского языка США и английского языка Новой Зеландии, используются дополнительно в в указанном порядке.
* Когда`ExactDateTimeParseFormats` содержит строки, они используются как дополнительные форматы даты-времени с использованием текущего языка и региональных параметров.
* Когда`ExactDateTimeParseFormats` пусто, дополнительные форматы даты и времени не используются.

### Смотрите также

* class [JsonDataLoadOptions](../)
* пространство имен [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* сборка [Aspose.Words](../../../)
