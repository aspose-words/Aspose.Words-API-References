---
title: ComparisonOperator
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает оператор сравнения.
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

Показывает, как пропускать страницы при слиянии с использованием поля SKIPIF.

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

// Создаем источник данных с 3 строками, одна из которых содержит «Джон Доу» в качестве значения для столбца «Имя».
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

// Создаем источник данных с 3 строками, одна из которых содержит «Джон Доу» в качестве значения для столбца «Имя».
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

* class [FieldSkipIf](../../fieldskipif)
* namespace [Aspose.Words.Fields](../../fieldskipif)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
