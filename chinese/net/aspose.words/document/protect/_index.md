---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words for .NET
description: 使用文档保护功能轻松保护您的文档。防止未经授权的更改，同时保留现有密码或使用随机密码。
type: docs
weight: 690
url: /zh/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

保护文档不被更改，无需更改现有密码或分配随机密码。

```csharp
public void Protect(ProtectionType type)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | ProtectionType | 指定文档的保护类型。 |

## 评论

当文档受到保护时，用户只能进行有限的更改，例如添加注释、进行修改或填写表格。

当您保护文档时，如果该文档已经有保护密码， 现有的保护密码不会改变。

当您保护文档时，如果该文档没有保护密码， 此方法会分配一个随机密码，使得无法在 Microsoft Word 中取消保护该文档 ，但您仍然可以在 Aspose.Words 中取消保护该文档，因为取消保护时不需要密码。

## 例子

显示如何关闭某个部分的保护。

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
// 并且我们只能编辑第二部分中的表单字段的内容。
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### 也可以看看

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

保护文档不被更改，并可选择设置保护密码。

```csharp
public void Protect(ProtectionType type, string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| type | ProtectionType | 指定文档的保护类型。 |
| password | String | 用于保护文档的密码。 指定`无效的`或者，如果您想不使用密码保护文档，则输入空字符串。 |

## 评论

当文档受到保护时，用户只能进行有限的更改，例如添加注释、进行修改或填写表格。

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
