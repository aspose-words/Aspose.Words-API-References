---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.Field — ваш ключ к улучшению документов Microsoft Word с помощью динамических полей для повышения функциональности и эффективности.
type: docs
weight: 1920
url: /ru/net/aspose.words.fields/field/
---
## Field class

Представляет поле документа Microsoft Word.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class Field
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/#update)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Поле в документе Word представляет собой сложную структуру, состоящую из нескольких узлов, которые включают начало поля, код поля, разделитель поля, результат поля и конец поля. Поля могут быть вложенными, содержать расширенный контент и охватывать несколько абзацев или разделов в документе.`Field` класс представляет собой объект «фасад», который предоставляет свойства и методы, позволяющие работать с полем как с единым объектом.

The[`Start`](./start/) ,[`Separator`](./separator/) и[`End`](./end/) свойства указывают на начальный, разделительный и конечный узлы поля the соответственно.

Содержимое между началом поля и разделителем — это код поля. Содержимое между разделителем поля the и концом поля — это результат поля. Код поля обычно состоит из одного или нескольких [`Run`](../../aspose.words/run/) объекты, которые определяют инструкции. Ожидается, что обрабатывающее приложение выполнит код поля для вычисления результата поля.

Процесс вычисления результатов поля называется обновлением поля. Aspose.Words может обновлять field результаты большинства типов полей точно так же, как это делает Microsoft Word. В частности, Aspose.Words может вычислять результаты даже самых сложных полей формул. Чтобы вычислить field результат одного поля, используйте[`Update`](./update/) метод. Для обновления полей во всем document используйте[`UpdateFields`](../../aspose.words/document/updatefields/).

Вы можете получить текстовую версию кода поля, используя[`GetFieldCode`](./getfieldcode/)method. Вы можете получить и задать текстовую версию результата поля, используя[`Result`](./result/) property. Как код поля, так и результат поля могут содержать сложный контент, такой как вложенные поля, абзацы, фигуры, таблицы, и в этом случае вам может потребоваться работать с узлами полей напрямую, если вам требуется больше контроля.

Вы не создаете экземпляры`Field` class напрямую. Чтобы создать новое поле, используйте[`InsertField`](../../aspose.words/documentbuilder/insertfield/) метод.

## Примеры

Показывает, как вставить поле в документ, используя код поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
