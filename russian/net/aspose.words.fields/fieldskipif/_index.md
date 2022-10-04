---
title: FieldSkipIf
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле SKIPIF.
type: docs
weight: 2270
url: /ru/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

Реализует поле SKIPIF.

```csharp
public class FieldSkipIf : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | Получает или задает оператор сравнения. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Получает или задает левую часть выражения сравнения. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Получает или задает правую часть выражения сравнения. |
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

Сравнивает значения, обозначенные выражениями[`LeftExpression`](./leftexpression/) а также[`RightExpression`](./rightexpression/) по сравнению с оператором, назначенным[`ComparisonOperator`](./comparisonoperator/) Если сравнение истинно, SKIPIF отменяет текущий документ слияния, переходит к следующей записи данных в источнике данных и запускает новый документ слияния. Если сравнение ложно, текущий документ слияния продолжается.

### Примеры

Показывает, как пропускать страницы при слиянии с помощью поля SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить поле SKIPIF. Если текущая строка операции слияния почты удовлетворяет условию
// которое указано в выражениях этого поля, то операция слияния прерывает текущую строку,
// отбрасывает текущий документ слияния, а затем сразу же переходит к следующей строке, чтобы начать следующий документ слияния.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Переместите построитель в разделитель поля SKIPIF, чтобы мы могли разместить MERGEFIELD внутри поля SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD относится к столбцу «Отдел» в нашей таблице данных. Если строка из этой таблицы
// имеет значение «HR» в столбце «Отдел», то эта строка будет соответствовать условию.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Добавляем содержимое в наш документ, создаем источник данных и выполняем слияние.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // В этой таблице три строки, и одна из них удовлетворяет условию нашего поля SKIPIF.
// Слияние почты создаст две страницы.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Показывает, как использовать поля MERGEREC и MERGESEQ для нумерации и подсчета записей слияния в выходных документах слияния.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Поле MERGEREC будет печатать номер строки объединяемых данных в каждом выходном документе слияния.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Поле MERGESEQ будет подсчитывать количество успешных слияний и печатать текущее значение на каждой соответствующей странице.
// Если слияние почты не пропускает ни одной строки и не вызывает поля SKIP/SKIPIF/NEXT/NEXTIF, то все слияния выполнены успешно.
// В полях MERGESEQ и MERGEREC будут отображаться те же результаты, что и слияние почты прошло успешно.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Вставьте поле SKIPIF, которое пропустит слияние, если имя "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Создайте источник данных с 3 строками, одна из которых содержит "Джон Доу" в качестве значения для столбца "Имя".
// Так как поле SKIPIF будет активировано этим значением один раз, вывод нашего слияния почты будет иметь 2 страницы вместо 3.
// На странице 1 в полях MERGESEQ и MERGEREC будет отображаться «1».
// На странице 2 в поле MERGEREC будет отображаться «3», а в поле MERGESEQ — «2».
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
