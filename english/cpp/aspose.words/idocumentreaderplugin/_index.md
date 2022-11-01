---
title: IDocumentReaderPlugin
second_title: Aspose.Words for C++ API Reference
description: Defines an interface for external reader plugins that can read a file into a document.
type: docs
weight: 989
url: /cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Defines an interface for external reader plugins that can read a file into a document.

```cpp
class IDocumentReaderPlugin : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Reads the data from the specified stream into the [Document](../document/) instance. |
