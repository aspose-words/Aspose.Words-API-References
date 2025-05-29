---
title: FieldBidiOutline Class
linktitle: FieldBidiOutline
articleTitle: FieldBidiOutline
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldBidiOutline для бесшовной реализации полей BIDIOUTLINE, расширяя возможности обработки документов.
type: docs
weight: 2060
url: /ru/net/aspose.words.fields/fieldbidioutline/
---
## FieldBidiOutline class

Реализует поле BIDIOUTLINE.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldBidiOutline : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldBidiOutline](fieldbidioutline/)() | Конструктор по умолчанию. |

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Это поле идентично полю AUTONUMLGL, за исключением разделителя, который разграничивает каждый уровень нумерации абзацев.

## Примеры

Показывает, как создавать списки с написанием справа налево, совместимые с языками, с полями BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле BIDIOUTLINE нумерует абзацы, как поля AUTONUM/LISTNUM,
// но виден только при включенном языке редактирования с письмом справа налево, например иврите или арабском.
// В следующем поле будет отображаться «.1», эквивалент RTL номера списка «1.».
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Добавьте еще два поля BIDIOUTLINE, которые будут отображать «.2» и «.3».
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Устанавливаем горизонтальное выравнивание текста для каждого абзаца в документе на RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Если мы включим в Microsoft Word язык редактирования с написанием справа налево, в наших полях будут отображаться числа.
// В противном случае будет отображаться «###».
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
