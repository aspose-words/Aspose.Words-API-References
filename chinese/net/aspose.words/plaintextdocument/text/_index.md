---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 访问 PlainTextDocument 的文本属性以将文档的内容作为单个字符串检索，从而增强数据处理和分析。
type: docs
weight: 40
url: /zh/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

获取文档的文本内容，并将其连接为字符串。

```csharp
public string Text { get; }
```

## 例子

展示如何以纯文本形式加载 Microsoft Word 文档的内容。

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### 也可以看看

* class [PlainTextDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
