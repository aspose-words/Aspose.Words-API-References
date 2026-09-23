---
title: "IAiModelText"
linktitle: "IAiModelText"
second_title: "Aspose.Words for Java"
description: "用于在 Java 中生成各种基于文本内容的 AI 模型的通用接口。"
type: docs
weight: 748
url: /zh/java/com.aspose.words/iaimodeltext/
---
```
public interface IAiModelText
```

用于生成各种基于文本内容的 AI 模型的通用接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [checkGrammar(Document sourceDocument, CheckGrammarOptions options)](#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions) | 检查提供的文档的语法。 |
| [summarize(Document sourceDocument, SummarizeOptions options)](#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions) | 生成指定文档的摘要，并提供调整摘要长度的选项。 |
| [summarize(Document[] sourceDocuments, SummarizeOptions options)](#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions) | 为一组文档生成摘要，并提供控制摘要长度及其他设置的选项。 |
| [translate(Document sourceDocument, int targetLanguage)](#translate-com.aspose.words.Document-int) |  |
### checkGrammar(Document sourceDocument, CheckGrammarOptions options) {#checkGrammar-com.aspose.words.Document-com.aspose.words.CheckGrammarOptions}
```
public abstract Document checkGrammar(Document sourceDocument, CheckGrammarOptions options)
```


检查提供的文档的语法。此操作利用已连接的 AI 模型来检查文档的语法。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | 正在检查语法的文档。 |
| options | [CheckGrammarOptions](../../com.aspose.words/checkgrammaroptions/) | 用于控制语法检查方式的可选设置。 |

**Returns:**
[Document](../../com.aspose.words/document/) - A new [Document](../../com.aspose.words/document/) with checked grammar.
### summarize(Document sourceDocument, SummarizeOptions options) {#summarize-com.aspose.words.Document-com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document sourceDocument, SummarizeOptions options)
```


生成指定文档的摘要，并提供调整摘要长度的选项。此操作利用已连接的 AI 模型进行内容处理。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) | 待摘要的文档。 |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | 用于控制摘要长度及其他参数的可选设置。 |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### summarize(Document[] sourceDocuments, SummarizeOptions options) {#summarize-com.aspose.words.Document---com.aspose.words.SummarizeOptions}
```
public abstract Document summarize(Document[] sourceDocuments, SummarizeOptions options)
```


为一组文档生成摘要，并提供控制摘要长度及其他设置的选项。此方法利用已连接的 AI 模型处理数组中的每个文档。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocuments | [Document\[\]](../../com.aspose.words/document/) | 待摘要的一组文档。 |
| options | [SummarizeOptions](../../com.aspose.words/summarizeoptions/) | 用于控制摘要长度及其他参数的可选设置 |

**Returns:**
[Document](../../com.aspose.words/document/) - A summarized version of the document's content.
### translate(Document sourceDocument, int targetLanguage) {#translate-com.aspose.words.Document-int}
```
public abstract Document translate(Document sourceDocument, int targetLanguage)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | [Document](../../com.aspose.words/document/) |  |
| targetLanguage | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
