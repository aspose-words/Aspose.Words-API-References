---
title: GoogleAiModel class
linktitle: GoogleAiModel class
articleTitle: GoogleAiModel class
second_title: Aspose.Words for Python
description: "aspose.words.ai.GoogleAiModel class. Class representing Google AI Models (Gemini) integration within Aspose.Words."
type: docs
weight: 50
url: /python-net/aspose.words.ai/googleaimodel/
---

## GoogleAiModel class

Class representing Google AI Models (Gemini) integration within Aspose.Words.


### Remarks

Please refer to https://ai.google.dev/gemini-api/docs/models for Gemini models details.


**Inheritance:** [GoogleAiModel](./) → [AiModel](../aimodel/)

### Constructors
| Name | Description |
| --- | --- |
| [GoogleAiModel(name)](./__init__/#str) | Initializes a new instance of [GoogleAiModel](./) class. |
| [GoogleAiModel(name, api_key)](./__init__/#str_str) | Initializes a new instance of [GoogleAiModel](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [timeout](../aimodel/timeout/) | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds).<br>(Inherited from [AiModel](../aimodel/)) |
| [url](./url/) | Gets or sets a URL of the model. The default value is "https://generativelanguage.googleapis.com/v1beta/models/". |

### Methods

| Name | Description |
| --- | --- |
|[ check_grammar(source_document, options)](../aimodel/check_grammar/#document_checkgrammaroptions) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document.<br>(Inherited from [AiModel](../aimodel/)) |
|[ create(model_type)](../aimodel/create/#aimodeltype) | Creates a new instance of [AiModel](../aimodel/) class.<br>(Inherited from [AiModel](../aimodel/)) |
|[ summarize(doc, options)](./summarize/#document_summarizeoptions) | Summarizes specified [Document](../../aspose.words/document/) object. |
|[ summarize(docs, options)](./summarize/#documentlist_summarizeoptions) | Summarizes specified [Document](../../aspose.words/document/) objects. |
|[ translate(doc, language)](./translate/#document_language) | Translates a specified document. |
|[ with_api_key(api_key)](../aimodel/with_api_key/#str) | Sets a specified API key to the model.<br>(Inherited from [AiModel](../aimodel/)) |

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

Shows how to use google AI model.

```python
api_key = system_helper.environment.Environment.get_environment_variable('API_KEY')
model = aw.ai.GoogleAiModel(name='gemini-flash-latest', api_key=api_key)
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
summarize_options = aw.ai.SummarizeOptions()
summarize_options.summary_length = aw.ai.SummaryLength.VERY_SHORT
summary = model.summarize(doc=doc, options=summarize_options)
```

### See Also

* module [aspose.words.ai](../)
* class [AiModel](../aimodel/)

