---
title: Aspose::Words::Saving::IPageSavingCallback interface
linktitle: IPageSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::IPageSavingCallback interface. Implement this interface if you want to control how Aspose.Words saves separate pages when saving a document to fixed page formats in C++.'
type: docs
weight: 44000
url: /cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Implement this interface if you want to control how Aspose.Words saves separate pages when saving a document to fixed page formats.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Called when Aspose.Words saves a separate page to fixed page formats. |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
