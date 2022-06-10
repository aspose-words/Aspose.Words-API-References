---
title: Field
second_title: Справочник по API Aspose.Words для .NET
description: Представляет поле документа Microsoft Word.
type: docs
weight: 1340
url: /ru/net/aspose.words.fields/field/
---
## Field class

Представляет поле документа Microsoft Word.

```csharp
public class Field
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает объект[`FieldFormat`](../fieldformat), предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или устанавливает, заблокировано ли поле (не должно пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode#getfieldcode)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode#getfieldcode_1)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update#update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update#update_1)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Поле в документе Word представляет собой сложную структуру, состоящую из нескольких узлов, включая начало поля, код поля, разделитель полей, результат поля и конец поля. Поля могут быть вложенными, содержать расширенное содержимое и охватывать несколько абзацев или разделов в документе. Класс[`Field`](../field)представляет собой "фасадный" объект, предоставляющий свойства и методы, позволяющие работать с полем как с единым объектом.

[`Start`](./start),Separatorи[`End`](./end)указывают на начальный, разделительный и конечный узлы поля поля соответственно.

Содержимое между началом поля и разделителем является кодом поля. Содержимое между разделителем полей и концом поля является результатом поля. Код поля обычно состоит из одного или нескольких объектов [`Run`](../../aspose.words/run), которые определяют инструкции. Ожидается, что приложение обработки выполнит код поля для вычисления результата поля.

Процесс подсчета полевых результатов называется обновлением поля. Aspose.Words может обновлять поля результатов большинства типов полей точно так же, как это делает Microsoft Word. В частности, Aspose.Words может вычислять результаты даже самых сложных полей формулы. Для вычисления поля результата одного поля используйте метод[`Update`](./update). Чтобы обновить поля во всем документе используйте[`UpdateFields`](../../aspose.words/document/updatefields).

Вы можете получить текстовую версию кода поля, используя[`GetFieldCode`](./getfieldcode)метод. Вы можете получить и установить текстовую версию результата поля, используя свойство[`Result`](./result). И код поля, и результат поля могут содержать сложное содержимое, такое как вложенные поля, абзацы, формы, таблицы, и в этом случае вы можете напрямую работать с узлами полей. если вам нужно больше контроля.

Вы не создаете экземпляры класса[`Field`](../field)напрямую. Чтобы создать новое поле, используйте метод[`InsertField`](../../aspose.words/documentbuilder/insertfield).

### Примеры

Показывает, как вставить поле в документ, используя код поля.

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

* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
