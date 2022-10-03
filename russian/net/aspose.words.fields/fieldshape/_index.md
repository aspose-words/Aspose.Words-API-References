---
title: FieldShape
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле SHAPE.
type: docs
weight: 2260
url: /ru/net/aspose.words.fields/fieldshape/
---
## FieldShape class

Реализует поле SHAPE.

```csharp
public class FieldShape : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldShape](fieldshape/)() | Конструктор по умолчанию. |

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
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [Text](../../aspose.words.fields/fieldshape/text/) { get; set; } | Получает или задает текст для извлечения. |
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

Извлекает указанный текст.

### Примеры

Показывает, как создавать совместимые с языком списки с написанием справа налево с полями BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле BIDIOUTLINE нумерует абзацы, как поля AUTONUM/LISTNUM,
// но отображается только при включенном языке редактирования справа налево, таком как иврит или арабский.
// Следующее поле будет отображать ".1", RTL-эквивалент номера списка "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Добавьте еще два поля BIDIOUTLINE, которые будут отображать ".2" и ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Установить горизонтальное выравнивание текста для каждого абзаца в документе на RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Если мы включим язык редактирования справа налево в Microsoft Word, наши поля будут отображать числа.
// В противном случае они будут отображать "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Показывает, как некоторые старые поля Microsoft Word, такие как SHAPE и EMBED, обрабатываются во время загрузки.

```csharp
// Откройте документ, созданный в Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Если мы откроем документ Word и нажмем Alt+F9, мы увидим ФОРМУ и поле ВСТАВИТЬ.
// Поле SHAPE является якорем/холстом для объекта AutoShape с включенным стилем обтекания "В соответствии с текстом".
// Поле EMBED имеет ту же функцию, но для встроенного объекта
// например, электронная таблица из внешнего документа Excel.
// Однако эти поля не будут отображаться в коллекции Fields документа.
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

// Третья форма — это то, что было полем EMBED, содержащим внешнюю электронную таблицу.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
