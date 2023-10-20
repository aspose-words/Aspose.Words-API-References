---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words для .NET
description: FieldOptions LegacyNumberFormat свойство. Получает или задает значение указывающее включен или нет устаревший ранний чем AW 13.10 числовой формат для полей на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Получает или задает значение, указывающее, включен или нет устаревший (ранний, чем AW 13.10) числовой формат для полей.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Примечания

Когда для этого свойства установлено значение`истинный`, символ шаблона "#" работает как в .net: Заменяет знак решетки соответствующей цифрой, если она присутствует; в противном случае в строке результата не появятся никакие символы.

Когда для этого свойства установлено значение`ЛОЖЬ`, символ шаблона «#» работает как MS Word: Этот элемент формата определяет необходимые числовые позиции для отображения в результате. Если результат не содержит цифру в этом месте, MS Word отображает пробел. Например, { = 9 + 6 \# $### } отображает 15 долларов.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

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

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
