---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: 用于 .NET 的 Aspose.Words
description: WriteProtection ValidatePassword 方法. 返回真的如果指定的密码与保护文档的写保护密码相同 如果文档没有使用密码写保护则返回错误的 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

返回`真的`如果指定的密码与保护文档的写保护密码相同。 如果文档没有使用密码写保护，则返回`错误的`.

```csharp
public bool ValidatePassword(string password)
```

## 例子

演示如何使用密码保护文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// 输入长度不超过15个字符的密码，然后验证文档的保护状态。
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// 保护不会阻止以编程方式编辑文档，也不会加密内容。
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### 也可以看看

* class [WriteProtection](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
