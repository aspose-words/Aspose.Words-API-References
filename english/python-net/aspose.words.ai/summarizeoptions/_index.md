---
title: SummarizeOptions class
linktitle: SummarizeOptions class
articleTitle: SummarizeOptions class
second_title: Aspose.Words for Python
description: "aspose.words.ai.SummarizeOptions class. Allows to specify various options for summarizing document content."
type: docs
weight: 90
url: /python-net/aspose.words.ai/summarizeoptions/
---

## SummarizeOptions class

Allows to specify various options for summarizing document content.


### Constructors
| Name | Description |
| --- | --- |
| [SummarizeOptions()](./__init__/#default) | Initializes a new instances of [SummarizeOptions](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [summary_length](./summary_length/) | Allows to specify summary length. Default value is [SummaryLength.MEDIUM](../summarylength/#MEDIUM). |

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

