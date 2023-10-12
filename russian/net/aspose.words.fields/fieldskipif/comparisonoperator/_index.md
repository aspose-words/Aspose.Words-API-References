---
title: FieldSkipIf.ComparisonOperator
second_title: Справочник по API Aspose.Words для .NET
description: FieldSkipIf свойство. Получает или задает оператор сравнения.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

Получает или задает оператор сравнения.

```csharp
public string ComparisonOperator { get; set; }
```

### Примеры

Показывает, как пропускать страницы при слиянии писем с помощью поля SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле SKIPIF. Если текущая строка операции слияния почты соответствует условию
// что указывают выражения этого поля, то операция слияния почты прерывает текущую строку,
// отбрасывает текущий документ слияния, а затем немедленно переходит к следующей строке, чтобы начать следующий документ слияния.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Переместите построитель к разделителю поля SKIPIF, чтобы мы могли поместить MERGEFIELD внутри поля SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD относится к столбцу «Отдел» в нашей таблице данных. Если строка из этой таблицы
// имеет значение «HR» в столбце «Отдел», то эта строка будет соответствовать условию.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Добавляем содержимое в наш документ, создаем источник данных и выполняем слияние почты.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // В этой таблице три строки, и одна из них соответствует условию нашего поля SKIPIF.
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

Показывает, как использовать поля MERGEREC и MERGESEQ для подсчета количества записей слияния в выходных документах слияния.

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

// Поле MERGESEQ подсчитывает количество успешных слияний и печатает текущее значение на каждой соответствующей странице.
// Если слияние почты не пропускает ни одной строки и не вызывает поля SKIP/SKIPIF/NEXT/NEXTIF, то все слияния успешны.
// Поля MERGESEQ и MERGEREC будут отображать одинаковые результаты, если слияние почты прошло успешно.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Вставьте поле SKIPIF, которое пропустит слияние, если имя «Джон Доу».
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Создаем источник данных с тремя строками, в одной из которых в столбце «Имя» указано «Джон Доу».
// Поскольку поле SKIPIF будет активировано один раз по этому значению, выходные данные нашего слияния будут иметь 2 страницы вместо 3.
// На странице 1 в полях MERGESEQ и MERGEREC будет отображаться значение «1».
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

* class [FieldSkipIf](../)
* пространство имен [Aspose.Words.Fields](../../fieldskipif/)
* сборка [Aspose.Words](../../../)


