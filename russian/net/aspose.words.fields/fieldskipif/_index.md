---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldSkipIf для эффективной реализации полей SKIPIF, повышения автоматизации документов и гибкости ваших проектов.
type: docs
weight: 2830
url: /ru/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

Реализует поле SKIPIF.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

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
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Возвращает или задает левую часть выражения сравнения. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Возвращает или задает правую часть выражения сравнения. |
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

Сравнивает значения, обозначенные выражениями[`LeftExpression`](./leftexpression/) и[`RightExpression`](./rightexpression/) в сравнении с использованием оператора, обозначенного[`ComparisonOperator`](./comparisonoperator/) . Если сравнение истинно, SKIPIF отменяет текущий документ слияния, переходит к следующей записи данных в источнике данных и начинает новый документ слияния. Если сравнение ложно, текущий документ слияния продолжается.

## Примеры

Показывает, как пропускать страницы при слиянии почты с помощью поля SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле SKIPIF. Если текущая строка операции слияния почты удовлетворяет условию
// что выражения этого поля указывают, то операция слияния почты прерывает текущую строку,
// отменяет текущий документ слияния, а затем немедленно переходит к следующей строке, чтобы начать следующий документ слияния.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Перемещаем конструктор на разделитель поля SKIPIF, чтобы мы могли поместить MERGEFIELD внутрь поля SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD ссылается на столбец "Department" в нашей таблице данных. Если строка из этой таблицы
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
// В результате слияния будут созданы две страницы.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Показывает, как использовать поля MERGEREC и MERGESEQ для нумерации и подсчета записей слияния почты в выходных документах слияния почты.

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

// Поле MERGESEQ подсчитывает количество успешных слияний и выводит текущее значение на каждой соответствующей странице.
// Если при слиянии почты не пропускается ни одна строка и не вызываются поля SKIP/SKIPIF/NEXT/NEXTIF, то все слияния успешны.
// Поля MERGESEQ и MERGEREC отобразят одинаковые результаты, если их слияние прошло успешно.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Вставьте поле SKIPIF, которое пропустит объединение, если имя «John Doe».
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Создаем источник данных с 3 строками, одна из которых содержит «John Doe» в качестве значения столбца «Name».
// Поскольку поле SKIPIF будет активировано этим значением один раз, вывод нашего слияния будет содержать 2 страницы вместо 3.
// На странице 1 поля MERGESEQ и MERGEREC будут отображать «1».
// На странице 2 поле MERGEREC отобразит «3», а поле MERGESEQ отобразит «2».
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
