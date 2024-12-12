---
title: SummarizeOptions.summary_length property
linktitle: summary_length property
articleTitle: summary_length property
second_title: Aspose.Words for Python
description: "SummarizeOptions.summary_length property. Allows to specify summary length"
type: docs
weight: 20
url: /python-net/aspose.words.ai/summarizeoptions/summary_length/
---

## SummarizeOptions.summary_length property

Allows to specify summary length.
Default value is [SummaryLength.MEDIUM](../../summarylength/#MEDIUM).



```python
@property
def summary_length(self) -> aspose.words.ai.SummaryLength:
    ...

@summary_length.setter
def summary_length(self, value: aspose.words.ai.SummaryLength):
    ...

```

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

* module [aspose.words.ai](../../)
* class [SummarizeOptions](../)

