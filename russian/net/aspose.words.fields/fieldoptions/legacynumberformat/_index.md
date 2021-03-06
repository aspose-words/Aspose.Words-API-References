---
title: LegacyNumberFormat
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает значение указывающее включен ли устаревший более ранний чем AW 13.10 числовой формат для полей.
type: docs
weight: 140
url: /ru/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Получает или задает значение, указывающее, включен ли устаревший (более ранний, чем AW 13.10) числовой формат для полей.

```csharp
public bool LegacyNumberFormat { get; set; }
```

### Примечания

Когда это свойство установлено в **истинный**, шаблонный символ "#" работал как в .net: Заменяет знак решетки на соответствующую цифру, если она присутствует; в противном случае в результирующей строке символы не появляются.

Когда это свойство установлено в **ЛОЖЬ**, символ шаблона "#" работает как MS Word: Этот элемент формата определяет необходимые числовые позиции для отображения в результате. Если результат не содержит цифры в этом месте, MS Word отображает пробел. Например, { = 9 + 6 \# $### } отображает 15 долларов.

Значение по умолчанию **ЛОЖЬ**.

### Примеры

Показывает, как включить устаревшее форматирование чисел для полей.

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

* class [FieldOptions](../../fieldoptions)
* пространство имен [Aspose.Words.Fields](../../fieldoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
