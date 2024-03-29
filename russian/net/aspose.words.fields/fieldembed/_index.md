---
title: FieldEmbed Class
linktitle: FieldEmbed
articleTitle: FieldEmbed
second_title: Aspose.Words для .NET
description: Aspose.Words.Fields.FieldEmbed сорт. Реализует поле EMBED на С#.
type: docs
weight: 1850
url: /ru/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

Реализует поле EMBED.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public class FieldEmbed : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldEmbed](fieldembed/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, обеспечивающий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, расположенный между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Возможно`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

## Примеры

Показывает, как обрабатываются во время загрузки некоторые старые поля Microsoft Word, такие как SHAPE и EMBED.

```csharp
// Откройте документ, созданный в Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Если мы откроем документ Word и нажмем Alt+F9, мы увидим ФОРМУ и поле EMBED.
// Поле SHAPE — это привязка/холст для объекта AutoShape с включенным стилем переноса «В соответствии с текстом».
// Поле EMBED имеет ту же функцию, но для встроенного объекта:
// например, электронная таблица из внешнего документа Excel.
// Однако эти поля не появятся в коллекции Fields документа.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Эти поля поддерживаются только старыми версиями Microsoft Word.
// Процесс загрузки документа преобразует эти поля в объекты Shape,
// к которому мы можем получить доступ в коллекции узлов документа.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Первый узел Shape соответствует полю SHAPE во входном документе,
// который является встроенным холстом для автофигуры.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Второй узел Shape — это сама AutoShape.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Третья форма — это поле EMBED, содержащее внешнюю электронную таблицу.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
