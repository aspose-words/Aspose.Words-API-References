---
title: Aspose::Words::AI::IAiModelText::Translate method
linktitle: Translate
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::IAiModelText::Translate method. Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.ai/iaimodeltext/translate/
---
## IAiModelText::Translate method


Translates the provided document into the specified target language. This operation leverages the connected [AI](../../) model for content translating.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::IAiModelText::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | The document to be translated. |
| targetLanguage | Aspose::Words::AI::Language | The language into which the document will be translated. |

### ReturnValue

A new [Document](../../../aspose.words/document/) object containing the translated document.

## See Also

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Interface [IAiModelText](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
