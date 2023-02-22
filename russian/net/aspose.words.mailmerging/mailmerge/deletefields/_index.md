---
title: MailMerge.DeleteFields
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge метод. Удаляет поля связанные со слиянием из документа.
type: docs
weight: 170
url: /ru/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Удаляет поля, связанные со слиянием, из документа.

```csharp
public void DeleteFields()
```

### Примечания

Этот метод удаляет поля MERGEFIELD и NEXT из документа.

Этот метод может быть полезен, если ваша операция слияния не всегда требует для заполнения всех полей в документе. Используйте этот метод, чтобы удалить все поля слияния rest .

### Примеры

Показывает, как удалить все поля MERGEFIELD из документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)


