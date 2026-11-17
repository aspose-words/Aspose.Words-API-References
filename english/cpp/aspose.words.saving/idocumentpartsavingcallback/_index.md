---
title: Aspose::Words::Saving::IDocumentPartSavingCallback interface
linktitle: IDocumentPartSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::IDocumentPartSavingCallback interface. Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to Html or Epub format in C++.'
type: docs
weight: 40000
url: /cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Implement this interface if you want to receive notifications and control how Aspose.Words saves document parts when exporting a document to [Html](../../aspose.words/saveformat/) or [Epub](../../aspose.words/saveformat/) format.

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Called when Aspose.Words is about to save a document part. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
