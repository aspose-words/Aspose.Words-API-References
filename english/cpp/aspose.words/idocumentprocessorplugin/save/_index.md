---
title: Aspose::Words::IDocumentProcessorPlugin::Save method
linktitle: Save
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentProcessorPlugin::Save method. Save the document loaded by Load() method to the output stream using the specified save options in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin::Save method


Save the document loaded by [Load()](../load/) method to the output stream using the specified save options.

```cpp
virtual void Aspose::Words::IDocumentProcessorPlugin::Save(System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | The output stream. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | The save options. |
## Remarks

If the specified output format is image, only the first page image is saved to the output stream. If the specified save format is not natively supported by the plugin (requires loading to [Document](../../document/)), method throws an exception.
## See Also

* Interface [IDocumentProcessorPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
