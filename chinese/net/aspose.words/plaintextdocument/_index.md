---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PlainTextDocument 类，轻松从文档中提取和利用纯文本，以增强可读性和处理能力。
type: docs
weight: 5170
url: /zh/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

允许提取文档内容的纯文本表示。

要了解更多信息，请访问[使用文本文档](https://docs.aspose.com/words/net/working-with-text-document/)文档文章。

```csharp
public class PlainTextDocument
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | 从流创建纯文本文档。自动检测文件格式。 |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | 从文件创建纯文本文档。自动检测文件格式。 |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 从流创建纯文本文档。允许指定其他选项，例如加密密码。 |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | 从文件创建纯文本文档。允许指定其他选项，例如加密密码。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | 获取[`BuiltInDocumentProperties`](./builtindocumentproperties/)的文件。 |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | 获取[`CustomDocumentProperties`](./customdocumentproperties/)的文件。 |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | 获取文档的文本内容，并将其连接为字符串。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
