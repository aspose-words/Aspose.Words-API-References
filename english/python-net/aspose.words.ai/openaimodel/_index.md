---
title: OpenAiModel class
linktitle: OpenAiModel class
articleTitle: OpenAiModel class
second_title: Aspose.Words for Python
description: "aspose.words.ai.OpenAiModel class. An abstract class representing the integration with OpenAI's large language models within the Aspose.Words."
type: docs
weight: 50
url: /python-net/aspose.words.ai/openaimodel/
---

## OpenAiModel class

An abstract class representing the integration with OpenAI's large language models within the Aspose.Words.


**Inheritance:** [OpenAiModel](./) → [AiModel](../aimodel/)

**Interfaces:** [IAiModelText](../iaimodeltext/)

### Methods

| Name | Description |
| --- | --- |
|[ create(model_type)](../aimodel/create/#aimodeltype) | Creates a new instance of [AiModel](../aimodel/) class.<br>(Inherited from [AiModel](../aimodel/)) |
|[ summarize(doc, options)](../iaimodeltext/summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.<br>(Inherited from [IAiModelText](../iaimodeltext/)) |
|[ summarize(docs, options)](../iaimodeltext/summarize/#documentlist_summarizeoptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.<br>(Inherited from [IAiModelText](../iaimodeltext/)) |
|[ with_api_key(api_key)](../aimodel/with_api_key/#str) | Sets a specified API key to the model.<br>(Inherited from [AiModel](../aimodel/)) |
|[ with_organization(organization_id)](./with_organization/#str) | Sets a specified Organization to the model. |
|[ with_project(project_id)](./with_project/#str) | Sets a specified Project to the model. |

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
* class [AiModel](../aimodel/)
* class [IAiModelText](../iaimodeltext/)

