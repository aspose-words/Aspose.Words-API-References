---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words для .NET
description: FieldOptions UseInvariantCultureNumberFormat свойство. Получает или задает значение указывающее что числовой формат анализируется с использованием инвариантного языка и региональных параметров или нет на С#.
type: docs
weight: 210
url: /ru/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Получает или задает значение, указывающее, что числовой формат анализируется с использованием инвариантного языка и региональных параметров или нет

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Примечания

Когда для этого свойства установлено значение`истинный` , числовой формат взят из инвариантного языка и региональных параметров.

Когда для этого свойства установлено значение`ЛОЖЬ` , числовой формат берется из культуры текущего потока.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как форматировать числа в соответствии с инвариантным языком и региональными параметрами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // Иногда поля могут неправильно форматировать свои числа в определенных культурах.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// Чтобы это исправить, мы могли бы изменить культуру для всего потока.
// Другой способ исправить это — установить этот флаг,
// который заставляет все поля использовать инвариантный язык и региональные параметры при форматировании чисел.
// Этот способ позволяет нам избежать изменения культуры для всего потока.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
