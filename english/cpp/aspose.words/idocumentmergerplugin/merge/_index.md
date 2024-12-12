---
title: Aspose::Words::IDocumentMergerPlugin::Merge method
linktitle: Merge
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentMergerPlugin::Merge method. Merges the given input PDF documents into a single output PDF document using specified input and output streams in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Merges the given input PDF documents into a single output PDF document using specified input and output streams.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | The output stream. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | The input streams. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | Load options for the input files. |

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
