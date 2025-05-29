---
title: CheckGrammarOptions Class
linktitle: CheckGrammarOptions
articleTitle: CheckGrammarOptions
second_title: Aspose.Words لـ .NET
description: حسّن مستنداتك مع خيارات Aspose.Words.AI.CheckGrammar. اكتشف تدقيقات قواعدية قابلة للتخصيص بتقنية الذكاء الاصطناعي لكتابة مثالية ووضوح أفضل.
type: docs
weight: 50
url: /ar/net/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class

يسمح بتحديد خيارات مختلفة أثناء التحقق من قواعد اللغة في المستند باستخدام الذكاء الاصطناعي.

```csharp
public class CheckGrammarOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CheckGrammarOptions](checkgrammaroptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ImproveStylistics](../../aspose.words.ai/checkgrammaroptions/improvestylistics/) { get; set; } | يسمح بتحديد ما إذا كان الذكاء الاصطناعي سيحاول تحسين أسلوب النص الذي تتم مراجعته. القيمة الافتراضية هي`خطأ شنيع` . |
| [MakeRevisions](../../aspose.words.ai/checkgrammaroptions/makerevisions/) { get; set; } | يسمح بتحديد المستند النهائي أو المنقح الذي سيتم إرجاعه مع نص منقح. القيمة الافتراضية هي`خطأ شنيع` . |
| [PreserveFormatting](../../aspose.words.ai/checkgrammaroptions/preserveformatting/) { get; set; } | يسمح بتحديد أي منهما[`CheckGrammar`](../iaimodeltext/checkgrammar/)سوف نحاول الحفاظ على تخطيط وتنسيق المستند الأصلي، أو لا. القيمة الافتراضية لـ هي`حقيقي` . |

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

* مساحة الاسم [Aspose.Words.AI](../../aspose.words.ai/)
* المجسم [Aspose.Words](../../)
