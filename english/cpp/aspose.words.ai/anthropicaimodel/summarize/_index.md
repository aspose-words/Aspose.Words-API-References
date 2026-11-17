---
title: Aspose::Words::AI::AnthropicAiModel::Summarize method
linktitle: Summarize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AnthropicAiModel::Summarize method. Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.ai/anthropicaimodel/summarize/
---
## AnthropicAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected [AI](../../) model for processing each document in the array.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | An array of documents to be summarized. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Optional settings to control the summary length and other parameters |

### ReturnValue

A summarized version of the document's content.

## See Also

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## AnthropicAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected [AI](../../) model for content processing.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | The document to be summarized. |
| options | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Optional settings to control the summary length and other parameters. |

### ReturnValue

A summarized version of the document's content.

## See Also

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
