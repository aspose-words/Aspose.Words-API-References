---
title: FieldNext Class
linktitle: FieldNext
articleTitle: FieldNext
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldNext для эффективного управления полями NEXT в ваших документах. Улучшите автоматизацию документов сегодня!
type: docs
weight: 2590
url: /ru/net/aspose.words.fields/fieldnext/
---
## FieldNext class

Реализует поле NEXT.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldNext : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldNext](fieldnext/)() | Конструктор по умолчанию. |

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

Объединяет следующую запись данных в текущий результирующий объединенный документ, а не начинает новый объединенный документ.

## Примеры

Показывает, как использовать поля NEXT/NEXTIF для объединения нескольких строк на одной странице во время слияния почты.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Создаем источник данных для нашего слияния с 3 строками.
    // Слияние почты, использующее эту таблицу, обычно создает трехстраничный документ.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Если у нас есть несколько полей слияния с одинаковым FieldName,
    // они будут получать данные из одной и той же строки источника данных и отображать одно и то же значение после слияния.
    // Поле NEXT сообщает слиянию немедленно переместиться на одну строку вниз,
    // что означает, что любые поля MERGEFIELD, следующие за полем NEXT, получат данные из следующей строки.
    // Никогда не пытайтесь перейти к следующей строке, если вы уже находитесь на предыдущей строке.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // После слияния значения источника данных, которые принимают эти MERGEFIELD
     // окажется на той же странице, что и MERGEFIELD выше.
    InsertMergeFields(builder, "Second row: ");

    // Поле NEXTIF имеет ту же функцию, что и поле NEXT,
    // но он переходит к следующей строке только в том случае, если утверждение, составленное на основе следующих 3 свойств, является истинным.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Если сравнение, подтвержденное указанным выше полем, верно,
    // следующие 3 поля слияния будут брать данные из третьей строки.
    // В противном случае эти поля снова возьмут данные из строки 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Наш источник данных содержит 3 строки, и мы пропустили строки дважды.
    // Наш выходной документ будет иметь 1 страницу с данными из всех 3 строк.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Использует конструктор документов для вставки полей MERGEFIELD для источника данных, содержащего столбцы с именами «Courtesy Title», «First Name» и «Last Name».
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Использует конструктор документов для вставки MERRGEFIELD с указанными свойствами.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
