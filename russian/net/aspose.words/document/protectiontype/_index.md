---
title: Document.ProtectionType
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает текущий активный тип защиты документа.
type: docs
weight: 310
url: /ru/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Получает текущий активный тип защиты документа.

```csharp
public ProtectionType ProtectionType { get; }
```

### Примечания

Это свойство позволяет получить текущий установленный тип защиты документа. Для изменения типа защиты документа используйте кнопку[`Protect`](../protect/) и[`Unprotect`](../unprotect/)методы.

Когда документ защищен, пользователь может вносить только ограниченные изменения, , такие как добавление аннотаций, внесение изменений или заполнение формы.

Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи задается с помощью[`WriteProtection`](../writeprotection/)

### Примеры

Показывает, как защитить и снять защиту с документа.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Если мы откроем этот документ в Microsoft Word, намереваясь его отредактировать,
// нам нужно будет применить пароль, чтобы пройти защиту.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Обратите внимание, что защита распространяется только на пользователей Microsoft Word, открывающих наш документ.
// Мы никак не зашифровали документ, и нам не нужен пароль, чтобы открыть и отредактировать его программно.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Есть два способа снять защиту с документа.
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
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


