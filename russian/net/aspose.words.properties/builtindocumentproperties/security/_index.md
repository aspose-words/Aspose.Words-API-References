---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words для .NET
description: Откройте для себя функцию BuiltInDocumentProperties Security, точно определяющую уровень безопасности вашего документа. Улучшите защиту вашего документа сегодня!
type: docs
weight: 270
url: /ru/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Указывает уровень безопасности документа в виде числового значения.

```csharp
public DocumentSecurity Security { get; set; }
```

## Примечания

Используйте это свойство только в информационных целях, поскольку Microsoft Word не всегда устанавливает это свойство. Это свойство доступно только в документах DOC и OOXML.

Чтобы защитить или снять защиту документа, используйте the [`Protect`](../../../aspose.words/document/protect/) и[`Unprotect`](../../../aspose.words/document/unprotect/) методы.

Aspose.Words обновляет это свойство до правильного значения перед сохранением документа.

## Примеры

Показывает, как использовать свойства документа для отображения уровня безопасности документа.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Если мы настроим документ как доступный только для чтения, он отобразит этот статус с помощью встроенного свойства «Безопасность».
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Защитите документ от записи, а затем проверьте его уровень безопасности.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Безопасность" — описательное свойство. Мы можем редактировать его значение вручную.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Смотрите также

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
