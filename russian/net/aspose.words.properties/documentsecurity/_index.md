---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.DocumentSecurity, чтобы повысить безопасность вашего документа. Легко указывайте и управляйте уровнями безопасности для оптимальной защиты.
type: docs
weight: 5220
url: /ru/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Используется как значение для[`Security`](../builtindocumentproperties/security/) свойство. Указывает уровень безопасности документа в виде числового значения.

```csharp
[Flags]
public enum DocumentSecurity
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Свойство не определяет состояния безопасности. |
| PasswordProtected | `1` | Документ защищен паролем. (Примечание еще ни разу не встречалось в документе). |
| ReadOnlyRecommended | `2` | Документ должен быть открыт только для чтения, если это возможно, но эту настройку можно переопределить. |
| ReadOnlyEnforced | `4` | Документ, который всегда будет открываться только для чтения. |
| ReadOnlyExceptAnnotations | `8` | Документ всегда будет открываться только для чтения, за исключением аннотаций. |

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

* пространство имен [Aspose.Words.Properties](../../aspose.words.properties/)
* сборка [Aspose.Words](../../)
