---
title: PlainTextDocument.Text
second_title: Aspose.Words for .NET API 参考
description: PlainTextDocument 财产. 获取连接为字符串的文档文本内容
type: docs
weight: 40
url: /zh/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

获取连接为字符串的文档文本内容。

```csharp
public string Text { get; }
```

### 例子

演示如何以纯文本形式加载 Microsoft Word 文档的内容。

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
* 命名空间 [Aspose.Words](../../plaintextdocument/)
* 部件 [Aspose.Words](../../../)


