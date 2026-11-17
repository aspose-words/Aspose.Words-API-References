---
title: Aspose::Words::Loading::IResourceLoadingCallback interface
linktitle: IResourceLoadingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::IResourceLoadingCallback interface. Implement this interface if you want to control how Aspose.Words loads external resource when importing a document and inserting images using DocumentBuilder in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Implement this interface if you want to control how Aspose.Words loads external resource when importing a document and inserting images using [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Called when Aspose.Words loads any external resource. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
