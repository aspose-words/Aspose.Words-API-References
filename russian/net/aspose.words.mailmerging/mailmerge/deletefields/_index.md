---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: Aspose.Words для .NET
description: MailMerge DeleteFields метод. Удаляет из документа поля связанные со слиянием почты на С#.
type: docs
weight: 170
url: /ru/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Удаляет из документа поля, связанные со слиянием почты.

```csharp
public void DeleteFields()
```

## Примечания

Этот метод удаляет из документа поля MERGEFIELD и NEXT.

Этот метод может быть полезен, если вашей операции слияния почты не всегда требуется для заполнения всех полей в документе. Используйте этот метод, чтобы удалить все поля слияния оставшейся почты .

## Примеры

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
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
