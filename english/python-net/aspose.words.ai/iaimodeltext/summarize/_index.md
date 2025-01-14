---
title: IAiModelText.summarize method
linktitle: summarize method
articleTitle: summarize method
second_title: Aspose.Words for Python
description: "aspose.words.ai.IAiModelText.summarize method"
type: docs
weight: 20
url: /python-net/aspose.words.ai/iaimodeltext/summarize/
---

## summarize(source_document, options) {#document_summarizeoptions}

Generates a summary of the specified document, with options to adjust the length of the summary.
This operation leverages the connected AI model for content processing.


```python
def summarize(self, source_document: aspose.words.Document, options: aspose.words.ai.SummarizeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_document | [Document](../../../aspose.words/document/) | The document to be summarized. |
| options | [SummarizeOptions](../../summarizeoptions/) | Optional settings to control the summary length and other parameters. |

### Returns

A summarized version of the document's content.


## summarize(source_documents, options) {#documentlist_summarizeoptions}

Generates summaries for an array of documents, with options to control the summary length and other settings.
This method utilizes the connected AI model for processing each document in the array.


```python
def summarize(self, source_documents: List[aspose.words.Document], options: aspose.words.ai.SummarizeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_documents | List[[Document](../../../aspose.words/document/)] | An array of documents to be summarized. |
| options | [SummarizeOptions](../../summarizeoptions/) | Optional settings to control the summary length and other parameters |

### Returns

A summarized version of the document's content.


## Examples

Shows how to summarize text using OpenAI and Google models.

```python
first_doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
second_doc = aw.Document(file_name=MY_DIR + 'Document.docx')
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
# Use OpenAI or Google generative language models.
model = aw.ai.AiModel.create(aw.ai.AiModelType.GPT_4O_MINI).with_api_key(api_key).as_open_ai_model().with_organization('Organization').with_project('Project')
options = aw.ai.SummarizeOptions()
options.summary_length = aw.ai.SummaryLength.SHORT
one_document_summary = model.summarize(source_document=first_doc, options=options)
one_document_summary.save(file_name=ARTIFACTS_DIR + 'AI.AiSummarize.One.docx')
options.summary_length = aw.ai.SummaryLength.LONG
multi_document_summary = model.summarize(source_documents=[first_doc, second_doc], options=options)
multi_document_summary.save(file_name=ARTIFACTS_DIR + 'AI.AiSummarize.Multi.docx')
```

## See Also

* module [aspose.words.ai](../../)
* class [IAiModelText](../)

