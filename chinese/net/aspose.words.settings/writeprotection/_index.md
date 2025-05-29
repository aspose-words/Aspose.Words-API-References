---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Settings.WriteProtection 类，轻松管理文档写保护设置并增强文档安全性。
type: docs
weight: 6800
url: /zh/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

指定文档的写保护设置。

要了解更多信息，请访问[保护或加密文档](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/)文档文章。

```csharp
public class WriteProtection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | 返回`真的`当设置了写保护密码时。 |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | 指定文档作者是否建议以只读方式打开文档。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | 设置文档的写保护密码。 |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | 返回`真的`如果指定的密码与文档的写保护密码相同。 如果文档未使用密码进行写保护，则返回`错误的`. |

## 评论

写保护指定作者是否建议以只读方式打开文档 和/或需要密码才能修改文档。

写保护与文档保护不同。写保护是在“另存为”对话框的选项中，在“ Microsoft Word”中指定的。

您不能直接创建此类的实例。您可以通过以下方式访问文档保护设置 [`WriteProtection`](../../aspose.words/document/writeprotection/)财产。

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

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
