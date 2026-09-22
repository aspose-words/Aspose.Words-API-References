---
title: "CheckGrammarOptions"
linktitle: "CheckGrammarOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات مختلفة أثناء فحص قواعد اللغة لمستند باستخدام الذكاء الاصطناعي في Java."
type: docs
weight: 101
url: /ar/java/com.aspose.words/checkgrammaroptions/
---

**Inheritance:**
java.lang.Object
```
public class CheckGrammarOptions
```

يسمح بتحديد خيارات مختلفة أثناء فحص قواعد اللغة لمستند باستخدام الذكاء الاصطناعي.

 **Examples:** 

يوضح كيفية فحص قواعد اللغة لمستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getImproveStylistics()](#getImproveStylistics) | يسمح بتحديد ما إذا كان الذكاء الاصطناعي سيحاول تحسين الأسلوب للنص الجاري تدقيقه. |
| [getMakeRevisions()](#getMakeRevisions) | يسمح بتحديد ما إذا كان المستند النهائي أو المعدل سيُعاد مع النص المدقق. |
| [getPreserveFormatting()](#getPreserveFormatting) | يسمح بتحديد ما إذا كان [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) سيحاول الحفاظ على تخطيط وتنسيق المستند الأصلي أم لا. |
| [setImproveStylistics(boolean value)](#setImproveStylistics-boolean) | يسمح بتحديد ما إذا كان الذكاء الاصطناعي سيحاول تحسين الأسلوب للنص الجاري تدقيقه. |
| [setMakeRevisions(boolean value)](#setMakeRevisions-boolean) | يسمح بتحديد ما إذا كان المستند النهائي أو المعدل سيُعاد مع النص المدقق. |
| [setPreserveFormatting(boolean value)](#setPreserveFormatting-boolean) | يسمح بتحديد ما إذا كان [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) سيحاول الحفاظ على تخطيط وتنسيق المستند الأصلي أم لا. |
### getImproveStylistics() {#getImproveStylistics}
```
public boolean getImproveStylistics()
```


يسمح بتحديد ما إذا كان الذكاء الاصطناعي سيحاول تحسين الأسلوب للنص الجاري تدقيقه. القيمة الافتراضية هي false.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getMakeRevisions() {#getMakeRevisions}
```
public boolean getMakeRevisions()
```


يسمح بتحديد ما إذا كان المستند النهائي أو المعدل يُعاد مع النص المُدقق. القيمة الافتراضية هي false.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getPreserveFormatting() {#getPreserveFormatting}
```
public boolean getPreserveFormatting()
```


يسمح بتحديد ما إذا كان [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) سيحاول الحفاظ على تخطيط وتنسيق المستند الأصلي، أم لا. القيمة الافتراضية هي true.

 **Remarks:** 

عند ضبط الخيار على false، تكون جودة تدقيق القواعد أعلى مقارنةً عندما يكون الخيار مضبوطًا على true. ومع ذلك، لا يتم الحفاظ على تنسيق النص الأصلي في هذه الحالة.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setImproveStylistics(boolean value) {#setImproveStylistics-boolean}
```
public void setImproveStylistics(boolean value)
```


يسمح بتحديد ما إذا كان الذكاء الاصطناعي سيحاول تحسين الأسلوب للنص الجاري تدقيقه. القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setMakeRevisions(boolean value) {#setMakeRevisions-boolean}
```
public void setMakeRevisions(boolean value)
```


يسمح بتحديد ما إذا كان المستند النهائي أو المعدل يُعاد مع النص المُدقق. القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setPreserveFormatting(boolean value) {#setPreserveFormatting-boolean}
```
public void setPreserveFormatting(boolean value)
```


يسمح بتحديد ما إذا كان [AiModel.checkGrammar(com.aspose.words.Document, com.aspose.words.CheckGrammarOptions)](../../com.aspose.words/aimodel/\#checkGrammar-com.aspose.words.Document--com.aspose.words.CheckGrammarOptions) سيحاول الحفاظ على تخطيط وتنسيق المستند الأصلي، أم لا. القيمة الافتراضية هي true.

 **Remarks:** 

عند ضبط الخيار على false، تكون جودة تدقيق القواعد أعلى مقارنةً عندما يكون الخيار مضبوطًا على true. ومع ذلك، لا يتم الحفاظ على تنسيق النص الأصلي في هذه الحالة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

