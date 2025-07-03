---
title: Aspose::Words::Saving::ICssSavingCallback interface
linktitle: ICssSavingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ICssSavingCallback interface. Implement this interface if you want to control how Aspose.Words saves CSS (Cascading Style Sheet) when saving a document to HTML in C++.'
type: docs
weight: 39000
url: /cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


Implement this interface if you want to control how Aspose.Words saves CSS (Cascading [Style](../../aspose.words/style/) Sheet) when saving a document to HTML.

```cpp
class ICssSavingCallback : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | Called when Aspose.Words saves an CSS (Cascading [Style](../../aspose.words/style/) Sheet). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
