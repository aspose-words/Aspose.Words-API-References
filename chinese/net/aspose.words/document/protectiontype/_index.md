---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: 用于 .NET 的 Aspose.Words
description: Document ProtectionType 财产. 获取当前活动的文档保护类型 在 C#.
type: docs
weight: 330
url: /zh/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

获取当前活动的文档保护类型。

```csharp
public ProtectionType ProtectionType { get; }
```

## 评论

此属性允许检索当前设置的文档保护类型。 要更改文档保护类型，请使用[`Protect`](../protect/) 和[`Unprotect`](../unprotect/)方法。

当文档受到保护时，用户只能进行有限的更改，例如添加注释、进行修订或填写表单。

请注意，文档保护与写保护不同。 写保护是使用[`WriteProtection`](../writeprotection/)

## 例子

展示如何保护和取消保护文档。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 如果我们使用 Microsoft Word 打开此文档并打算对其进行编辑，
// 我们需要应用密码才能通过保护。
doc.Save(ArtifactsDir + "Document.Protect.docx");

// 请注意，保护仅适用于打开我们文档的 Microsoft Word 用户。
// 我们没有以任何方式加密文档，并且我们不需要密码即可以编程方式打开和编辑它。
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// 有两种方法可以删除文档的保护。
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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
