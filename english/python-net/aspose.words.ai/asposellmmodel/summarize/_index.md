---
title: AsposeLlmModel.summarize method
linktitle: summarize method
articleTitle: summarize method
second_title: Aspose.Words for Python
description: "aspose.words.ai.AsposeLlmModel.summarize method"
type: docs
weight: 30
url: /python-net/aspose.words.ai/asposellmmodel/summarize/
---

## summarize(source_document, options) {#document_summarizeoptions}

Generates a summary of the specified document, with options to adjust the length of the summary.


```python
def summarize(self, source_document: aspose.words.Document, options: aspose.words.ai.SummarizeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_document | [Document](../../../aspose.words/document/) |  |
| options | [SummarizeOptions](../../summarizeoptions/) |  |

## summarize(source_documents, options) {#documentlist_summarizeoptions}

Generates a summary for an array of documents, with options to adjust the length of the summary.


```python
def summarize(self, source_documents: List[aspose.words.Document], options: aspose.words.ai.SummarizeOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_documents | List[[Document](../../../aspose.words/document/)] |  |
| options | [SummarizeOptions](../../summarizeoptions/) |  |

## Examples

Shows how to summarize documents with a local model, so the content never leaves the machine.

```python
# Aspose.LLM is a separate package with its own license, for example:
# new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
first_doc = aw.Document(file_name=MY_DIR + "Big document.docx")
second_doc = aw.Document(file_name=MY_DIR + "Document.docx")
# Disposing the model releases the local model and its native resources.
with aw.ai.AsposeLlmModel("Qwen25_3BPresetCpu") as model:
    summarize_options = aw.ai.SummarizeOptions()
    summarize_options.summary_length = aw.ai.SummaryLength.SHORT
    summary = model.summarize(source_document=first_doc, options=summarize_options)
    summary.save(file_name=ARTIFACTS_DIR + "AI.AsposeLlmSummarize.One.docx")
    summarize_options.summary_length = aw.ai.SummaryLength.MEDIUM
    combined_summary = model.summarize(source_documents=[first_doc, second_doc], options=summarize_options)
    combined_summary.save(file_name=ARTIFACTS_DIR + "AI.AsposeLlmSummarize.Multiple.docx")
```

## See Also

* module [aspose.words.ai](../../)
* class [AsposeLlmModel](../)

