---
title: IAiModelText.CheckGrammar
linktitle: CheckGrammar
articleTitle: CheckGrammar
second_title: Aspose.Words لـ .NET
description: حسّن كتابتك باستخدام أداة التدقيق النحوي من IAiModelText. حسّن دقة مستنداتك بسهولة باستخدام تقنية التدقيق النحوي المتقدمة بالذكاء الاصطناعي.
type: docs
weight: 10
url: /ar/net/aspose.words.ai/iaimodeltext/checkgrammar/
---
## IAiModelText.CheckGrammar method

يتحقق من قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل للتحقق من قواعد اللغة للمستند.

```csharp
public Document CheckGrammar(Document sourceDocument, CheckGrammarOptions options = null)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sourceDocument | Document | الوثيقة التي يتم التحقق من قواعدها النحوية. |
| options | CheckGrammarOptions | إعدادات اختيارية للتحكم في كيفية التحقق من القواعد النحوية. |

### قيمة الإرجاع

جديد[`Document`](../../../aspose.words/document/) مع التدقيق النحوي.

## أمثلة

يوضح كيفية التحقق من قواعد اللغة في المستند.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// استخدم نماذج اللغة التوليدية OpenAI.
IAiModelText model = (OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

CheckGrammarOptions grammarOptions = new CheckGrammarOptions();
grammarOptions.ImproveStylistics = true;

Document proofedDoc = model.CheckGrammar(doc, grammarOptions);
proofedDoc.Save(ArtifactsDir + "AI.AiGrammar.docx");
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [CheckGrammarOptions](../../checkgrammaroptions/)
* interface [IAiModelText](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
