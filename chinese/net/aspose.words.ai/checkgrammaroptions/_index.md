---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.AI.CheckGrammarOptions 优化您的文档。探索可自定义的 AI 语法检查，实现完美写作，提升清晰度。
type: docs
weight: 50
url: /zh/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

允许在使用 AI 检查文档语法时指定各种选项。

```csharp
public class CheckGrammarOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | 允许指定 AI 将尝试改进正在校对的文本的风格。 默认值为`错误的`. |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | 允许指定返回最终或修订文档以及校对文本。 默认值为`错误的`. |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | 允许指定[`CheckGrammar`](../iaimodeltext/checkgrammar/)将尝试保留 原始文档的布局和格式，否则不保留。 默认值为`真的`. |

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

* 命名空间 [Aspose.Words.AI](../../aspose.words.ai/)
* 部件 [Aspose.Words](../../)
