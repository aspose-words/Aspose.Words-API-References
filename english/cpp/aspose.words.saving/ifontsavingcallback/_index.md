---
title: Aspose::Words::Saving::IFontSavingCallback interface
linktitle: IFontSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::IFontSavingCallback interface. Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format.

```cpp
class IFontSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | Called when Aspose.Words is about to save a font resource. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
