---
title: FieldMergeField.TextAfter
linktitle: TextAfter
articleTitle: TextAfter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldMergeField TextAfter, которое позволяет легко настраивать выводимые поля с помощью динамического текста, повышая ясность и вовлеченность документа.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldmergefield/textafter/
---
## FieldMergeField.TextAfter property

Возвращает или задает текст, который будет вставлен после поля, если поле не пустое.

```csharp
public string TextAfter { get; set; }
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

* class [FieldMergeField](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
