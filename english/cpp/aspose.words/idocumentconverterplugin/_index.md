---
title: Aspose::Words::IDocumentConverterPlugin interface
linktitle: IDocumentConverterPlugin
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentConverterPlugin interface. Defines an interface for external converter plugin in C++.'
type: docs
weight: 76250
url: /cpp/aspose.words/idocumentconverterplugin/
---
## IDocumentConverterPlugin interface


Defines an interface for external converter plugin.

```cpp
class IDocumentConverterPlugin : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Convert](./convert/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Converts document using specified input output streams and save options. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
