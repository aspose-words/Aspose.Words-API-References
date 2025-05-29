---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words for .NET
description: 使用我们的文档解除保护方法轻松解锁您的文档，删除任何密码保护以便于访问和编辑。
type: docs
weight: 790
url: /zh/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

无论密码是什么，都会删除文档的保护。

```csharp
public void Unprotect()
```

## 评论

即使文档有保护密码，此方法也会取消文档的保护。

请注意，文档保护不同于写保护。 写保护是使用[`WriteProtection`](../writeprotection/)。

## 例子

展示如何保护和取消保护文档。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 如果我们用 Microsoft Word 打开此文档并打算编辑它，
// 我们需要使用密码来突破保护。
doc.Save(ArtifactsDir + "Document.Protect.docx");

// 请注意，该保护仅适用于打开我们文档的 Microsoft Word 用户。
// 我们没有以任何方式加密该文档，并且我们不需要密码即可通过编程打开和编辑它。
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// 有两种方法可以取消文档的保护。
// 1 - 没有密码：
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - 使用正确的密码：
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

如果指定了正确的密码，则删除文档的保护。

```csharp
public bool Unprotect(string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | String | 用于取消文档保护的密码。 |

### 返回值

`真的`如果指定了正确的密码并且文档未受保护。

## 评论

仅当指定了正确的密码时，此方法才会取消对文档的保护。

请注意，文档保护不同于写保护。 写保护是使用[`WriteProtection`](../writeprotection/)。

## 例子

展示如何保护和取消保护文档。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 如果我们用 Microsoft Word 打开此文档并打算编辑它，
// 我们需要使用密码来突破保护。
doc.Save(ArtifactsDir + "Document.Protect.docx");

// 请注意，该保护仅适用于打开我们文档的 Microsoft Word 用户。
// 我们没有以任何方式加密该文档，并且我们不需要密码即可通过编程打开和编辑它。
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// 有两种方法可以取消文档的保护。
// 1 - 没有密码：
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - 使用正确的密码：
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
