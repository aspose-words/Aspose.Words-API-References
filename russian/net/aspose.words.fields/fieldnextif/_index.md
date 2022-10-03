---
title: FieldNextIf
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле NEXTIF.
type: docs
weight: 2040
url: /ru/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Реализует поле NEXTIF.

```csharp
public class FieldNextIf : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Получает или задает оператор сравнения. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Получает или задает левую часть выражения сравнения. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Получает или задает правую часть выражения сравнения. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
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

Сравнивает значения, обозначенные выражениями[`LeftExpression`](./leftexpression/) а также[`RightExpression`](./rightexpression/) по сравнению с оператором, назначенным[`ComparisonOperator`](./comparisonoperator/) . Если сравнение истинно, следующая запись данных объединяется с текущим документом слияния. (Поля слияния, которые следуют за NEXTIF в документе main , заменяются значениями из следующей записи данных, а не из текущей записи данных.) Если сравнение ложно, следующая запись данных объединяется с новым документом слияния.

### Примеры

Показывает, как использовать поля NEXT/NEXTIF для объединения нескольких строк в одну страницу во время слияния почты.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Создадим источник данных для нашего слияния с 3 строками.
    // Слияние почты, использующее эту таблицу, обычно создает 3-страничный документ.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Если у нас есть несколько полей слияния с одним и тем же FieldName,
    // они будут получать данные из той же строки источника данных и отображать одно и то же значение после слияния.
    // Поле NEXT указывает почтовому слиянию немедленно перейти на одну строку вниз,
    // что означает, что любые поля MERGEFIELD, которые следуют за полем NEXT, будут получать данные из следующей строки.
    // Убедитесь, что вы никогда не пытаетесь перейти к следующей строке, когда уже находитесь в последней строке.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // После слияния значения источника данных, которые принимают эти поля MERGEFIELD
     // окажется на той же странице, что и поля MERGEFIELD выше.
    InsertMergeFields(builder, "Second row: ");

    // Поле NEXTIF имеет ту же функцию, что и поле NEXT,
    // но он переходит к следующей строке только в том случае, если утверждение, созданное следующими тремя свойствами, истинно.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Если сравнение, подтвержденное указанным выше полем, корректно,
    // следующие 3 поля слияния возьмут данные из третьей строки.
    // В противном случае эти поля снова будут брать данные из строки 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // В нашем источнике данных 3 строки, и мы дважды пропустили строки.
    // Наш выходной документ будет иметь 1 страницу с данными из всех 3-х строк.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");

/// <summary>
/// Использует построитель документов для вставки полей MERGEFIELD для источника данных, который содержит столбцы с именами "Courtesy Title", "First Name" и "Last Name".
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
