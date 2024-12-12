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
|[ summarize(source_document, options)](./summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
|[ summarize(source_documents, options)](./summarize/#documentlist_summarizeoptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
|[ translate(source_document, target_language)](./translate/#document_language) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |

### Examples

Shows how to summarize text using OpenAI and Google models.

```python
first_doc = aw.Document(file_name=MY_DIR + "Big document.docx")
second_doc = aw.Document(file_name=MY_DIR + "Document.docx")
api_key = system_helper.environment.Environment.get_environment_variable("API_KEY")
# Use OpenAI or Google generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key).as_open_ai_model()
options = aw.ai.SummarizeOptions()
options.summary_length = aw.ai.SummaryLength.SHORT
one_document_summary = model.summarize(source_document=first_doc, options=options)
one_document_summary.save(file_name=ARTIFACTS_DIR + "AI.AiSummarize.One.docx")
options.summary_length = aw.ai.SummaryLength.LONG
multi_document_summary = model.summarize(source_documents=[first_doc, second_doc], options=options)
multi_document_summary.save(file_name=ARTIFACTS_DIR + "AI.AiSummarize.Multi.docx")
```

### See Also

* module [aspose.words.ai](../)

