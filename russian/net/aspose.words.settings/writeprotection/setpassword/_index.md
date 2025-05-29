---
title: WriteProtection.SetPassword
linktitle: SetPassword
articleTitle: SetPassword
second_title: Aspose.Words для .NET
description: Защитите свои документы с помощью метода WriteProtection SetPassword. Легко установите пароль для повышения безопасности документов и предотвращения несанкционированного доступа.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

Устанавливает пароль защиты от записи для документа.

```csharp
public void SetPassword(string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | String | Пароль для установки. Не может быть`нулевой`, но может быть пустой строкой. |

## Примечания

Если установлен пароль, Microsoft Word потребует от пользователя ввести его или открыть документ только для чтения.

## Примеры

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

// Защита не препятствует программному редактированию документа и не шифрует его содержимое.
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
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
