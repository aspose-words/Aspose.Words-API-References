---
title: IAiModelText class
linktitle: IAiModelText class
articleTitle: IAiModelText class
second_title: Aspose.Words for Python
description: "aspose.words.ai.IAiModelText class. The common interface for AI models designed to generate a variety of text-based content."
type: docs
weight: 40
url: /python-net/aspose.words.ai/iaimodeltext/
---

## IAiModelText class

The common interface for AI models designed to generate a variety of text-based content.


### Methods

| Name | Description |
| --- | --- |
|[ summarize(doc, options)](./summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
|[ summarize(docs, options)](./summarize/#documentlist_summarizeoptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |

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

