---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldOptions UseInvariantCultureNumberFormat, позволяющее легко управлять форматированием чисел с использованием инвариантной культуры для единообразной обработки данных.
type: docs
weight: 210
url: /ru/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

Возвращает или задает значение, указывающее, анализируется ли числовой формат с использованием инвариантной культуры или нет

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## Примечания

Когда это свойство установлено в`истинный` числовой формат взят из инвариантной культуры.

Когда это свойство установлено в`ЛОЖЬ` , числовой формат берется из культуры текущего потока.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как форматировать числа в соответствии с инвариантными региональными параметрами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // Иногда поля могут некорректно форматировать свои числа в определенных культурах.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// Чтобы исправить это, мы могли бы изменить культуру для всего потока.
// Другой способ исправить это — установить этот флаг,
// который заставляет все поля использовать инвариантную культуру при форматировании чисел.
// Этот способ позволяет нам избежать изменения культуры для всего потока.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
