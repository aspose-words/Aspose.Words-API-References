---
title: Read
second_title: Aspose.Words for C++ API Reference
description: Reads the data from the specified stream into the Document instance.
type: docs
weight: 1
url: /cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin.Read method


Reads the data from the specified stream into the [Document](../../document/) instance.

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Parameter | Type | Description |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | The source stream to read the document from. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | An additional load options to load the document. |
| document | System::SharedPtr\<Aspose::Words::Document\> | The instance of the [Document](../../document/) class to read the data to. If the instance contains some content, it will be overridden by the data from the source stream |


