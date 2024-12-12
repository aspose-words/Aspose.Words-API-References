---
title: Aspose::Words::IDocumentConverterPlugin::ConvertToImages method
linktitle: ConvertToImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentConverterPlugin::ConvertToImages method. Converts pages from document from input stream to array of images in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Converts pages from document from input stream to array of images.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | The input stream. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | The document load options. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | The save options. |

### ReturnValue

Array of page images streams.

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
