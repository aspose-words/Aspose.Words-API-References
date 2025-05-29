---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words для .NET
description: Откройте для себя тип активной защиты документов для повышения безопасности и целостности данных. Защитите свои файлы без усилий с помощью наших расширенных функций.
type: docs
weight: 340
url: /ru/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Получает текущий активный тип защиты документа.

```csharp
public ProtectionType ProtectionType { get; }
```

## Примечания

Это свойство позволяет получить текущий установленный тип защиты документа. Чтобы изменить тип защиты документа, используйте[`Protect`](../protect/) и[`Unprotect`](../unprotect/) методы.

Если документ защищен, пользователь может вносить только ограниченные изменения, например, добавлять аннотации, вносить исправления или заполнять формы.

Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи указывается с помощью[`WriteProtection`](../writeprotection/)

## Примеры

Показывает, как защитить и снять защиту документа.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Если мы откроем этот документ в Microsoft Word, намереваясь его редактировать,
// нам нужно будет применить пароль, чтобы обойти защиту.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Обратите внимание, что защита распространяется только на пользователей Microsoft Word, открывающих наш документ.
// Мы никак не зашифровали документ, и нам не нужен пароль для его программного открытия и редактирования.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Существует два способа снятия защиты с документа.
// 1 - Без пароля:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - С правильным паролем:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Смотрите также

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
