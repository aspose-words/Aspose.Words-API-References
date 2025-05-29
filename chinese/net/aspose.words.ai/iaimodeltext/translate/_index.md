---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words for .NET
description: 使用我们的 IAiModelText 翻译方法，轻松翻译文档。利用 AI 技术，以您所需的语言进行准确、快速的翻译。
type: docs
weight: 30
url: /zh/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

将提供的文档翻译成指定的目标语言。 此操作利用连接的 AI 模型进行内容翻译。

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | Document | 需要翻译的文件。 |
| targetLanguage | Language | 文档将被翻译成的语言。 |

### 返回值

一个新的[`Document`](../../../aspose.words/document/)包含翻译文档的对象。

## 例子

展示如何使用 Google 模型翻译文本。

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// 使用 Google 生成语言模型。
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)
