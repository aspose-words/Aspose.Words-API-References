---
title: AiModel class
linktitle: AiModel class
articleTitle: AiModel class
second_title: Aspose.Words for Python
description: "aspose.words.ai.AiModel class. An abstract class representing the integration with various AI models within the Aspose.Words."
type: docs
weight: 10
url: /python-net/aspose.words.ai/aimodel/
---

## AiModel class

An abstract class representing the integration with various AI models within the Aspose.Words.


### Methods

| Name | Description |
| --- | --- |
|[ as_anthropic_ai_model()](./as_anthropic_ai_model/#default) | Cast AiModel to [AnthropicAiModel](../anthropicaimodel/). |
|[ as_google_ai_model()](./as_google_ai_model/#default) | Cast AiModel to [GoogleAiModel](../googleaimodel/). |
|[ as_open_ai_model()](./as_open_ai_model/#default) | Cast AiModel to [OpenAiModel](../openaimodel/). |
|[ check_grammar(source_document, options)](./check_grammar/#document_checkgrammaroptions) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
|[ create(model_type)](./create/#aimodeltype) | Creates a new instance of [AiModel](./) class. |
|[ summarize(source_document, options)](./summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
|[ summarize(source_documents, options)](./summarize/#documentlist_summarizeoptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
|[ translate(source_document, target_language)](./translate/#document_language) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |
|[ with_api_key(api_key)](./with_api_key/#str) | Sets a specified API key to the model. |

### Examples

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

### See Also

* module [aspose.words.ai](../)

