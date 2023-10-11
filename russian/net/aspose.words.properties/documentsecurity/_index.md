---
title: Enum DocumentSecurity
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Properties.DocumentSecurity перечисление. Используется как значение дляSecurity property. Указывает уровень безопасности документа в виде числового значения.
type: docs
weight: 4490
url: /ru/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Используется как значение для[`Security`](../builtindocumentproperties/security/) property. Указывает уровень безопасности документа в виде числового значения.

```csharp
[Flags]
public enum DocumentSecurity
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Для свойства не указаны состояния безопасности. |
| PasswordProtected | `1` | Документ защищен паролем. (Примечание пока ни разу не встречалось в документе). |
| ReadOnlyRecommended | `2` | Документ, который будет открыт только для чтения, если это возможно, но этот параметр можно переопределить. |
| ReadOnlyEnforced | `4` | Документ, который всегда будет открыт только для чтения. |
| ReadOnlyExceptAnnotations | `8` | Документ, который всегда открывается только для чтения, за исключением аннотаций. |

### Примеры

Показывает, как использовать свойства документа для отображения уровня безопасности документа.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Если мы настроим документ только для чтения, он будет отображать этот статус с помощью встроенного свойства «Безопасность».
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Защитить документ от записи, а затем проверить уровень его безопасности.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// «Безопасность» — описательное свойство. Мы можем редактировать его значение вручную.
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


