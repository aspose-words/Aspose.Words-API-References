---
title: Class FieldAutoNum
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldAutoNum сорт. Реализует поле AUTONUM.
type: docs
weight: 1430
url: /ru/net/aspose.words.fields/fieldautonum/
---
## FieldAutoNum class

Реализует поле AUTONUM.

```csharp
public class FieldAutoNum : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldAutoNum](fieldautonum/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonum/separatorcharacter/) { get; set; } | Получает или задает используемый символ-разделитель. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Вставляет автоматический номер.

### Примеры

Показывает, как нумеровать абзацы с помощью полей autonum.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждое поле AUTONUM отображает текущее значение счетчика полей AUTONUM,
// что позволяет нам автоматически нумеровать элементы, как в нумерованном списке.
// В этом поле будет отображаться число «1.».
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Знак-разделитель, который появляется в поле результата сразу после числа, по умолчанию является точкой.
// Если мы оставим это свойство пустым, наше второе поле AUTONUM будет отображать «2». в документе.
Assert.IsNull(field.SeparatorCharacter);

// Мы можем установить это свойство, чтобы применить первый символ его строки в качестве нового символа-разделителя.
// В этом случае в нашем поле AUTONUM теперь будет отображаться "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


