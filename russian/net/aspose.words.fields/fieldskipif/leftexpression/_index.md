---
title: FieldSkipIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldSkipIf LeftExpression, легко управляйте левой частью выражений сравнения для улучшенного контроля данных и гибкости.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldskipif/leftexpression/
---
## FieldSkipIf.LeftExpression property

Возвращает или задает левую часть выражения сравнения.

```csharp
public string LeftExpression { get; set; }
```

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

* class [FieldSkipIf](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
