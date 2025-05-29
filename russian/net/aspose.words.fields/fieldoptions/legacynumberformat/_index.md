---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldOptions LegacyNumberFormat, позволяющее включать или отключать устаревшие числовые форматы для полей, повышая совместимость и производительность.
type: docs
weight: 160
url: /ru/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Возвращает или задает значение, указывающее, включен ли устаревший (более ранний, чем AW 13.10) числовой формат для полей.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Примечания

Когда это свойство установлено в`истинный`, символ шаблона "#" работает как в .net: Заменяет знак фунта на соответствующую цифру, если она присутствует; в противном случае в результирующей строке не отображается никаких символов.

Когда это свойство установлено в`ЛОЖЬ`, символ шаблона "#" работает как MS Word: Этот элемент формата определяет необходимые числовые позиции для отображения в результате. Если результат не включает цифру в этой позиции, MS Word отображает пробел. Например, { = 9 + 6 \# $### } отображает $ 15.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как включить устаревшее числовое форматирование для полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
