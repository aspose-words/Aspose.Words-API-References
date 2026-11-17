---
title: Aspose::Words::IDocumentProcessorPlugin interface
linktitle: IDocumentProcessorPlugin
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentProcessorPlugin interface. Defines an interface for external document processor plugin in C++.'
type: docs
weight: 76750
url: /cpp/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface


Defines an interface for external document processor plugin.

```cpp
class IDocumentProcessorPlugin : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Append](./append/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Append the document loading it with the specified load options. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Load](./load/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>) | Load the document using the specified load options. |
| virtual [Save](./save/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Save the document loaded by [Load()](./load/) method to the output stream using the specified save options. |
| virtual [SetImageWatermark](./setimagewatermark/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>) | Adds image watermark on each page of the document loaded by [Load()](./load/) method. |
| virtual [SetTextWatermark](./settextwatermark/)(System::String, System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>) | Adds text watermark on each page of the document loaded by [Load()](./load/) method. |
| virtual [ToDocument](./todocument/)() | Parses the document loaded by [Load()](./load/) method into [Document](../document/) object. |
| virtual [ToPages](./topages/)(System::SharedPtr\<Aspose::Words::Saving::FixedPageSaveOptions\>) | Saves each page of the document loaded by [Load()](./load/) method using the specified fixed page save options. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
