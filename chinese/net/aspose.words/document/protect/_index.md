---
title: Document.Protect
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 在不更改现有密码或分配随机密码的情况下保护文档免受更改
type: docs
weight: 630
url: /zh/net/aspose.words/document/protect/
---
## Protect(ProtectionType) {#protect}

在不更改现有密码或分配随机密码的情况下保护文档免受更改。

```csharp
public void Protect(ProtectionType type)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | ProtectionType | 指定文档的保护类型。 |

### 评论

当文档受到保护时，用户只能进行有限的更改， ，例如添加注释、进行修订或填写表格。

当您保护文档，并且文档已经有保护密码时， 现有的保护密码不会更改。

当您保护文档，并且文档没有保护密码时， 此方法会分配一个随机密码，使得无法在 Microsoft Word 中取消保护文档 ，但您仍然可以在 Aspose.Words 中取消保护文档，因为它没有 取消保护时需要密码。

### 例子

显示如何关闭部分的保护。

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

// 关闭第一节的写保护。
doc.Sections[0].ProtectedForForms = false;

// 在这个输出文档中，我们将能够自由编辑第一部分，
// 我们只能在第二部分编辑表单域的内容。
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### 也可以看看

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## Protect(ProtectionType, string) {#protect_1}

保护文档不被更改，并可选择设置保护密码。

```csharp
public void Protect(ProtectionType type, string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | ProtectionType | 指定文档的保护类型。 |
| password | String | 用于保护文档的密码。 如果要在没有密码的情况下保护文档，请指定 null 或空字符串。 |

### 评论

当文档受到保护时，用户只能进行有限的更改， ，例如添加注释、进行修订或填写表格。

请注意，文档保护不同于写保护。 写保护是使用[`WriteProtection`](../writeprotection/).

### 例子

显示如何保护和取消保护文档。

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 如果我们使用 Microsoft Word 打开此文档并打算对其进行编辑，
// 我们需要应用密码才能通过保护。
doc.Save(ArtifactsDir + "Document.Protect.docx");

// 请注意，该保护仅适用于打开我们文档的 Microsoft Word 用户。
// 我们没有以任何方式加密文档，我们不需要密码以编程方式打开和编辑它。
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// 有两种方法可以从文档中删除保护。
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
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


