---
title: WriteProtection.ValidatePassword
second_title: Справочник по API Aspose.Words для .NET
description: WriteProtection метод. Возвращаетистинный если указанный пароль совпадает с паролем защиты от записи с помощью которого документ был защищен. Если документ не защищен паролем от записи возвращается значениеЛОЖЬ .
type: docs
weight: 40
url: /ru/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Возвращает`истинный` если указанный пароль совпадает с паролем защиты от записи, с помощью которого документ был защищен. Если документ не защищен паролем от записи, возвращается значение`ЛОЖЬ` .

```csharp
public bool ValidatePassword(string password)
```

### Примеры

Показывает, как защитить документ паролем.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Введите пароль длиной до 15 символов, а затем проверьте статус защиты документа.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// Защита не предотвращает программное редактирование документа и не шифрует его содержимое.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Смотрите также

* class [WriteProtection](../)
* пространство имен [Aspose.Words.Settings](../../writeprotection/)
* сборка [Aspose.Words](../../../)


