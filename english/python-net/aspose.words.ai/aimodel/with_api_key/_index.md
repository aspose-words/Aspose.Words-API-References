---
title: AiModel.with_api_key method
linktitle: with_api_key method
articleTitle: with_api_key method
second_title: Aspose.Words for Python
description: "AiModel.with_api_key method. Sets a specified API key to the model."
type: docs
weight: 40
url: /python-net/aspose.words.ai/aimodel/with_api_key/
---

## with_api_key(api_key) {#str}

Sets a specified API key to the model.


```python
def with_api_key(self, api_key: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| api_key | str |  |

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

