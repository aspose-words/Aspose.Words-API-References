---
title: FieldMergeField.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldMergeField Type, чтобы легко получить доступ к типам полей Microsoft Word и расширить возможности автоматизации документов.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/fieldmergefield/type/
---
## FieldMergeField.Type property

Получает тип поля Microsoft Word.

```csharp
public override FieldType Type { get; }
```

## Примеры

Показывает, как использовать поля MERGEFIELD для выполнения слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте таблицу данных, которая будет использоваться в качестве источника данных для слияния почты.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Вставьте MERGEFIELD со свойством FieldName, равным имени столбца в источнике данных.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Мы можем применить текст до и после значения, которое это поле принимает при слиянии.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

// Вставьте еще один MERGEFIELD для другого столбца в источнике данных.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Смотрите также

* enum [FieldType](../../fieldtype/)
* class [FieldMergeField](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
