---
title: AiModel class
linktitle: AiModel class
articleTitle: AiModel class
second_title: Aspose.Words for Python
description: "aspose.words.ai.AiModel class. Represents information about a Generative Language Model."
type: docs
weight: 10
url: /python-net/aspose.words.ai/aimodel/
---

## AiModel class

Represents information about a Generative Language Model.


### Methods

| Name | Description |
| --- | --- |
|[ as_google_ai_model()](./as_google_ai_model/#default) | Cast AiModel to [GoogleAiModel](../googleaimodel/). |
|[ as_open_ai_model()](./as_open_ai_model/#default) | Cast AiModel to [OpenAiModel](../openaimodel/). |
|[ create(model_type)](./create/#aimodeltype) | Creates a new instance of [AiModel](./) class. |
|[ with_api_key(api_key)](./with_api_key/#str) | Sets a specified API key to the model. |

### Examples

Shows how to summarize text using OpenAI and Google models.

```python
first_doc = aw.Document(MyDir + "Big document.docx")
second_doc = aw.Document(MyDir + "Document.docx")
api_key = os.getenv("API_KEY")
# Use OpenAI or Google generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key).as_open_ai_model()
options = aw.ai.SummarizeOptions()
options.summary_length = aw.ai.SummaryLength.SHORT
one_document_summary = model.summarize(first_doc, options)
oneDocumentSummary.save(ArtifactsDir + "AI.AiSummarize.One.docx")
options.summary_length = aw.ai.SummaryLength.LONG
multi_document_summary = model.summarize([first_doc, second_doc], options)
multiDocumentSummary.save(ArtifactsDir + "AI.AiSummarize.Multi.docx")
```

### See Also

* module [aspose.words.ai](../)

