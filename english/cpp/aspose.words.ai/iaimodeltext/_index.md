---
title: Aspose::Words::AI::IAiModelText interface
linktitle: IAiModelText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::IAiModelText interface. The common interface for AI models designed to generate a variety of text-based content in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.ai/iaimodeltext/
---
## IAiModelText interface


The common interface for [AI](../) models designed to generate a variety of text-based content.

```cpp
class IAiModelText : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Checks grammar of the provided document. This operation leverages the connected [AI](../) model for checking grammar of document. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected [AI](../) model for content processing. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected [AI](../) model for processing each document in the array. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Translates the provided document into the specified target language. This operation leverages the connected [AI](../) model for content translating. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
