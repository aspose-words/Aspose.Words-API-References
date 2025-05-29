---
title: WriteProtection.SetPassword
linktitle: SetPassword
articleTitle: SetPassword
second_title: Aspose.Words for .NET
description: 使用 WriteProtection SetPassword 方法保护您的文档。轻松设置密码，增强文档安全性，防止未经授权的访问。
type: docs
weight: 30
url: /zh/net/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection.SetPassword method

设置文档的写保护密码。

```csharp
public void SetPassword(string password)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | String | 要设置的密码。无法`无效的`，但可以是空字符串。 |

## 评论

如果设置了密码，Microsoft Word 将要求用户输入密码或以只读方式打开 文档。

## 例子

展示如何使用密码保护文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// 输入长度最多为 15 个字符的密码，然后验证文档的保护状态。
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
