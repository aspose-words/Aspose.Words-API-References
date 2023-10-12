---
title: Document.Unprotect
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Снимает защиту с документа независимо от пароля.
type: docs
weight: 760
url: /ru/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Снимает защиту с документа независимо от пароля.

```csharp
public void Unprotect()
```

### Примечания

Этот метод снимает защиту с документа, даже если у него есть пароль защиты.

Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи задается с помощью[`WriteProtection`](../writeprotection/).

### Примеры

Показывает, как защитить и снять защиту документа.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Если мы откроем этот документ в Microsoft Word, намереваясь его отредактировать,
// нам нужно будет применить пароль, чтобы пройти защиту.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Обратите внимание, что защита распространяется только на пользователей Microsoft Word, открывающих наш документ.
// Мы никак не зашифровали документ, и для его программного открытия и редактирования пароль нам не нужен.
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

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## Unprotect(string) {#unprotect}

Снимает защиту с документа, если указан правильный пароль.

```csharp
public bool Unprotect(string password)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | String | Пароль для снятия защиты с документа. |

### Возвращаемое значение

`истинный` если был указан правильный пароль и документ был незащищен.

### Примечания

Этот метод снимает защиту документа только в том случае, если указан правильный пароль.

Обратите внимание, что защита документа отличается от защиты от записи. Защита от записи задается с помощью[`WriteProtection`](../writeprotection/).

### Примеры

Показывает, как защитить и снять защиту документа.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Если мы откроем этот документ в Microsoft Word, намереваясь его отредактировать,
// нам нужно будет применить пароль, чтобы пройти защиту.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Обратите внимание, что защита распространяется только на пользователей Microsoft Word, открывающих наш документ.
// Мы никак не зашифровали документ, и для его программного открытия и редактирования пароль нам не нужен.
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

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


