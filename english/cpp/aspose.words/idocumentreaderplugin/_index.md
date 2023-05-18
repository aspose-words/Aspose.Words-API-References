---
title: Aspose::Words::IDocumentReaderPlugin interface
linktitle: IDocumentReaderPlugin
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentReaderPlugin interface. Defines an interface for external reader plugins that can read a file into a document in C++.'
type: docs
weight: 77000
url: /cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Defines an interface for external reader plugins that can read a file into a document.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Reads the data from the specified stream into the [Document](../document/) instance. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
