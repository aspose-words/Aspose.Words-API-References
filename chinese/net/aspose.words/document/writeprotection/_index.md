---
title: Document.WriteProtection
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 提供对文档写保护选项的访问
type: docs
weight: 480
url: /zh/net/aspose.words/document/writeprotection/
---
## Document.WriteProtection property

提供对文档写保护选项的访问。

```csharp
public WriteProtection WriteProtection { get; }
```

### 例子

显示如何使用密码保护文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");

// 输入最长 15 个字符的密码，然后验证文档的保护状态。
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

* class [WriteProtection](../../../aspose.words.settings/writeprotection/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


