---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words for .NET
description: 使用 IAiModelText 的 CheckGrammar 方法提升您的写作水平。使用先进的 AI 语法检查，轻松提升文档准确性。
type: docs
weight: 10
url: /zh/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

检查所提供文档的语法。 此操作利用连接的 AI 模型来检查文档的语法。

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sourceDocument | Document | 正在检查语法的文档。 |
| options | CheckGrammarOptions | 可选设置来控制如何检查语法。 |

### 返回值

一个新的[`Document`](../../../aspose.words/document/)已检查语法。

## 例子

展示如何检查文档的语法。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// 使用 OpenAI 生成语言模型。
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### 也可以看看

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* 命名空间 [Aspose.Words.AI](../../../aspose.words.ai/)
* 部件 [Aspose.Words](../../../)
