---
title: Aspose::Words::Saving::IDocumentSavingCallback interface
linktitle: IDocumentSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::IDocumentSavingCallback interface. Implement this interface if you want to have your own custom method called during saving a document in C++.'
type: docs
weight: 41000
url: /cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Implement this interface if you want to have your own custom method called during saving a document.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | This is called to notify of document saving progress. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
