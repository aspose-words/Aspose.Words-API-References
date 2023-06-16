---
title: Aspose::Words::IDocumentMergerPlugin interface
linktitle: IDocumentMergerPlugin
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::IDocumentMergerPlugin interface. Defines an interface for external merger plugin that can merge Pdf documents in C++.'
type: docs
weight: 76500
url: /cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


Defines an interface for external merger plugin that can merge Pdf documents.

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&) | Merges the given input PDF documents into a single output PDF document using specified input and output streams. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
