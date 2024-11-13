---
title: AiModel.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "AiModel.create method. Creates a new instance of [AiModel](../) class."
type: docs
weight: 30
url: /python-net/aspose.words.ai/aimodel/create/
---

## create(model_type) {#aimodeltype}

Creates a new instance of [AiModel](../) class.



```python
def create(self, model_type: aspose.words.ai.AiModelType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| model_type | [AiModelType](../../aimodeltype/) |  |

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

* module [aspose.words.ai](../../)
* class [AiModel](../)

