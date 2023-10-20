---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.PlainTextDocument 班级. 允许提取文档内容的纯文本表示形式 在 C#.
type: docs
weight: 4440
url: /zh/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

允许提取文档内容的纯文本表示形式。

要了解更多信息，请访问[处理文本文档](https://docs.aspose.com/words/net/working-with-text-document/)文档文章。

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
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | 获取[`BuiltInDocumentProperties`](./builtindocumentproperties/)文档的. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | 获取[`CustomDocumentProperties`](./customdocumentproperties/)文档的. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | 获取连接为字符串的文档文本内容。 |

## 例子

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
