---
title: Aspose::Words::Saving::IResourceSavingCallback interface
linktitle: IResourceSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::IResourceSavingCallback interface. Implement this interface if you want to control how Aspose.Words saves external resources (images, fonts and css) when saving a document to fixed page HTML or SVG in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Implement this interface if you want to control how Aspose.Words saves external resources (images, fonts and css) when saving a document to fixed page HTML or SVG.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
