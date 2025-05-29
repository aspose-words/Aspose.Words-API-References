---
title: IAiModelText.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words لـ .NET
description: ترجم مستنداتك بسهولة باستخدام أسلوبنا للترجمة IAiModelText. استخدم الذكاء الاصطناعي لترجمة دقيقة وسريعة باللغة التي تريدها.
type: docs
weight: 30
url: /ar/net/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText.Translate method

يترجم المستند المقدم إلى لغة الهدف المحددة. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لترجمة المحتوى.

```csharp
public Document Translate(Document sourceDocument, Language targetLanguage)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sourceDocument | Document | الوثيقة المراد ترجمتها. |
| targetLanguage | Language | اللغة التي سيتم ترجمة المستند إليها. |

### قيمة الإرجاع

جديد[`Document`](../../../aspose.words/document/)الكائن الذي يحتوي على المستند المترجم.

## أمثلة

يوضح كيفية ترجمة النص باستخدام نماذج Google.

```csharp
Document doc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// استخدم نماذج اللغة التوليدية من Google.
IAiModelText model = (GoogleAiModel)AiModel.Create(AiModelType.Gemini15Flash).WithApiKey(apiKey);

Document translatedDoc = model.Translate(doc, Language.Arabic);
translatedDoc.Save(ArtifactsDir + "AI.AiTranslate.docx");
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* interface [IAiModelText](../)
* مساحة الاسم [Aspose.Words.AI](../../../aspose.words.ai/)
* المجسم [Aspose.Words](../../../)
