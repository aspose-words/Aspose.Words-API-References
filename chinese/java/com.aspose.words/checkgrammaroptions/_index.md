---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words for Java"
description: "允许在使用 Java 的 AI 检查文档语法时指定各种选项。"
type: docs
weight: 101
url: /zh/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

允许在使用 AI 检查文档语法时指定各种选项。

 **Examples:** 

展示如何检查文档的语法。

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use OpenAI generative language models.
 AiModel model = AiModel.create(AiModelType.GPT_4_O_MINI).withApiKey(apiKey);

 CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
 grammarOptions.setImproveStylistics(true);

 Document proofedDoc = model.checkGrammar(doc, grammarOptions);
 proofedDoc.save(getArtifactsDir() + "AI.AiGrammar.docx");
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | 允许指定 AI 是否尝试改进被校对文本的文体。 |
| [getMakeRevisions()](#getMakeRevisions) | 允许指定返回的文档是最终版还是修订版，并包含已校对的文本。 |
| [getPreserveFormatting()](#getPreserveFormatting) | 允许指定 [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) 将尝试保留原始文档的布局和格式，或不保留。 |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | 允许指定 AI 是否尝试改进被校对文本的文体。 |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | 允许指定返回的文档是最终版还是修订版，并包含已校对的文本。 |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | 允许指定 [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) 将尝试保留原始文档的布局和格式，或不保留。 |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


允许指定 AI 是否尝试改进被校对文本的文体。默认值为 false。

**Returns:**
boolean - 相应的 boolean 值。
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


允许指定返回的文档是最终版还是修订版，并包含已校对的文本。默认值为 false。

**Returns:**
boolean - 相应的 boolean 值。
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


允许指定 [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) 将尝试保留原始文档的布局和格式，或不保留。默认值为 true。

 **Remarks:** 

当该选项设置为 false 时，语法检查的质量高于设置为 true 时。然而，在这种情况下，文本的原始格式将不被保留。

**Returns:**
boolean - 相应的 boolean 值。
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


允许指定 AI 是否尝试改进被校对文本的文体。默认值为 false。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


允许指定返回的文档是最终版还是修订版，并包含已校对的文本。默认值为 false。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


允许指定 [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) 将尝试保留原始文档的布局和格式，或不保留。默认值为 true。

 **Remarks:** 

当该选项设置为 false 时，语法检查的质量高于设置为 true 时。然而，在这种情况下，文本的原始格式将不被保留。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

