---
title: FieldAdvance Class
linktitle: FieldAdvance
articleTitle: FieldAdvance
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldAdvance для бесшовной реализации полей ADVANCE, которая без труда расширит ваши возможности обработки документов.
type: docs
weight: 1950
url: /ru/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Реализует поле ADVANCE.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldAdvance : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldAdvance](fieldadvance/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset/) { get; set; } | Возвращает или задает количество точек, на которое следует переместить вниз текст, следующий за полем. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition/) { get; set; } | Возвращает или задает количество точек, на которое текст, следующий за полем, должен быть перемещен по горизонтали от левого края столбца, рамки или текстового поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset/) { get; set; } | Возвращает или задает количество точек, на которое текст, следующий за полем, должен быть перемещен влево. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset/) { get; set; } | Возвращает или задает количество точек, на которое текст, следующий за полем, должен быть перемещен вправо. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset/) { get; set; } | Возвращает или задает количество точек, на которое следует переместить вверх текст, следующий за полем. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition/) { get; set; } | Возвращает или задает количество точек, на которое текст, следующий за полем, должен быть перемещен вертикально от верхнего края страницы. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Перемещает начальную точку, в которой отображается текст, лексически следующий за полем, вправо или влево, вверх или вниз или в определенное горизонтальное или вертикальное положение.

## Примеры

Показывает, как вставить поле ADVANCE и редактировать его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Ниже приведены два способа использования поля ADVANCE для настройки положения текста, следующего за ним.
// Эффекты поля ADVANCE продолжают применяться до тех пор, пока не закончится абзац,
// или другое поле ADVANCE обновляет значения смещения/координат.
// 1 - Укажите смещение направления:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Переместить текст в позицию, указанную координатами:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
