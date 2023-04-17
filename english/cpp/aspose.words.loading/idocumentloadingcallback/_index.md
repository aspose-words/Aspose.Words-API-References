---
title: Aspose::Words::Loading::IDocumentLoadingCallback interface
linktitle: IDocumentLoadingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::IDocumentLoadingCallback interface. Implement this interface if you want to have your own custom method called during loading a document in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Implement this interface if you want to have your own custom method called during loading a document.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | This is called to notify of document loading progress. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
