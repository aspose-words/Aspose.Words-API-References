---
title: AsposeLlmModel.Translate
linktitle: Translate
articleTitle: Translate
second_title: Aspose.Words for .NET
description: AsposeLlmModel Translate method. Translates the provided document into the specified target language.
type: docs
weight: 50
url: /net/aspose.words.ai/asposellmmodel/translate/
---
## AsposeLlmModel.Translate method

Translates the provided document into the specified target language.

```csharp
public override Document Translate(Document sourceDocument, Language targetLanguage)
```

## Remarks

Same approach as [`Translate`](../../openaimodel/translate/): the whole document is sent as one piece of text marked with run separators, to preserve the original formatting by restoring the translation back into the original runs. A small local model damages a run separator more often than a cloud model, so any run that could not be restored this way is translated again individually, by Language).

### See Also

* class [Document](../../../aspose.words/document/)
* enum [Language](../../language/)
* class [AsposeLlmModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
