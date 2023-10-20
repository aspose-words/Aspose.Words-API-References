---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words для .NET
description: Aspose.Words.Fields.Field сорт. Представляет поле документа Microsoft Word на С#.
type: docs
weight: 1510
url: /ru/net/aspose.words.fields/field/
---
## Field class

Представляет поле документа Microsoft Word.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public class Field
```

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/#update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

## Примечания

Поле в документе Word представляет собой сложную структуру, состоящую из нескольких узлов, которые включают начало поля, код поля , разделитель полей, результат поля и конец поля. Поля могут быть вложенными, содержать богатое содержимое и содержать несколько абзацев или разделов в документе.`Field` class — это «фасадный» объект, который предоставляет свойства и методы , позволяющие работать с полем как с единым объектом.

[`Start`](./start/) ,[`Separator`](./separator/) и[`End`](./end/) Свойства указывают на начальный, разделительный и конечный узлы поля the поля соответственно.

Содержимое между началом поля и разделителем представляет собой код поля. Содержимое между разделителем полей the и концом поля является результатом поля. Код поля обычно состоит из одного или нескольких [`Run`](../../aspose.words/run/) объекты, задающие инструкции. Ожидается, что приложение обработки выполнит код поля для вычисления результата поля.

Процесс расчета результатов поля называется обновлением поля. Aspose.Words может обновлять результаты field большинства типов полей точно так же, как это делает Microsoft Word. В частности, Aspose.Words может вычислять результаты даже самых сложных полей формул. Чтобы вычислить результат field для одного поля, используйте[`Update`](./update/) метод. Чтобы обновить поля во всем документе document , используйте[`UpdateFields`](../../aspose.words/document/updatefields/).

Вы можете получить текстовую версию кода поля, используя команду[`GetFieldCode`](./getfieldcode/) метод. Вы можете получить и установить текстовую версию результата поля, используя метод[`Result`](./result/) property. И код поля, и результат поля могут содержать сложное содержимое, такое как вложенные поля, абзацы, фигуры, таблицы , и в этом случае вы можете захотеть работать с узлами полей напрямую, если вам нужно больше контроля.

Вы не создаете экземпляры`Field` напрямую класс. Чтобы создать новое поле, используйте[`InsertField`](../../aspose.words/documentbuilder/insertfield/) метод.

## Примеры

Показывает, как вставить поле в документ с помощью кода поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
