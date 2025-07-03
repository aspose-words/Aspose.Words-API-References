---
title: Aspose::Words::Saving::IImageSavingCallback interface
linktitle: IImageSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::IImageSavingCallback interface. Implement this interface if you want to control how Aspose.Words saves images when saving a document to HTML. May be used by other formats in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Implement this interface if you want to control how Aspose.Words saves images when saving a document to HTML. May be used by other formats.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Called when Aspose.Words saves an image to HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
