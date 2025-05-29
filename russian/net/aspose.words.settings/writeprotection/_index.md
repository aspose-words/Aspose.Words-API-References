---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Settings.WriteProtection, который позволит легко управлять параметрами защиты документов от записи и повысить безопасность ваших документов.
type: docs
weight: 6800
url: /ru/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Задает параметры защиты от записи для документа.

Чтобы узнать больше, посетите[Защитить или зашифровать документ](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) документальная статья.

```csharp
public class WriteProtection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Возврат`истинный` когда установлен пароль защиты от записи. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Указывает, рекомендовал ли автор документа открывать документ только для чтения. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Устанавливает пароль защиты от записи для документа. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Возврат`истинный` если указанный пароль совпадает с паролем защиты от записи, которым был защищен документ. Если документ не защищен от записи паролем, то возвращается`ЛОЖЬ` . |

## Примечания

Защита от записи указывает, рекомендовал ли автор открывать документ только для чтения и/или требовать пароль для изменения документа.

Защита от записи отличается от защиты документа. Защита от записи указывается в Microsoft Word в параметрах диалогового окна Сохранить как.

Вы не создаете экземпляры этого класса напрямую. Вы получаете доступ к настройкам защиты документа через[`WriteProtection`](../../aspose.words/document/writeprotection/) свойство.

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

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
