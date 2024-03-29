---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: 用于 .NET 的 Aspose.Words
description: Document Protect 方法. 保护文档免遭更改而不更改现有密码或分配随机密码 在 C#.
type: docs
weight: 650
url: /zh/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

保护文档免遭更改，而不更改现有密码或分配随机密码。

```csharp
public void Protect(ProtectionType type)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | ProtectionType | 指定文档的保护类型。 |

## 评论

当文档受到保护时，用户只能进行有限的更改，例如添加注释、进行修订或填写表单。

当您保护文档且该文档已有保护密码时， 现有保护密码不会更改。

当您保护文档且该文档没有保护密码时， 此方法会分配一个随机密码，使得无法在 Microsoft Word 中取消对文档 的保护，但您仍然可以在 Aspose.Words 中取消对文档的保护，因为它不会 取消保护时需要密码。

## 例子

展示如何关闭某个部分的保护。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// 对文档中的每个部分应用写保护。
doc.Protect(ProtectionType.AllowOnlyFormFields);

// 关闭第一部分的写保护。
doc.Sections[0].ProtectedForForms = false;

// 在此输出文档中，我们将能够自由编辑第一部分，
// 我们只能编辑第二部分中表单字段的内容。
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### 也可以看看

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

保护文档免遭更改，并可选择设置保护密码。

```csharp
public void Protect(ProtectionType type, string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | ProtectionType | 指定文档的保护类型。 |
| password | String | 保护文档的密码用. 指定`无效的`如果您想在没有密码的情况下保护文档，则为空字符串。 |

## 评论

当文档受到保护时，用户只能进行有限的更改，例如添加注释、进行修订或填写表单。

请注意，文档保护与写保护不同。 写保护是使用[`WriteProtection`](../writeprotection/)。

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
