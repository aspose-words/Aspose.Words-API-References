---
title: Aspose::Words::Saving::CssSavingArgs class
linktitle: CssSavingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::CssSavingArgs class. Provides data for the CssSaving() event. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Provides data for the [CssSaving()](../icsssavingcallback/csssaving/) event. To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class CssSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Allows to specify the stream where the CSS information will be saved to. |
| [get_Document](./get_document/)() const | Gets the document object that is currently being saved. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is **true**. When this property is **false**, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving an CSS information. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Allows to specify whether the CSS will be exported to file and embedded to HTML document. Default is **true**. When this property is **false**, the CSS information will not be saved to a CSS file and will not be embedded to HTML document. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Setter for [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Remarks


By default, when Aspose.Words saves a document to HTML, it saves CSS information inline (as a value of the **style** attribute on every element).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

To save CSS into stream, use the [CssStream](./get_cssstream/) property.

To suppress saving CSS into a file and embedding to HTML document use the [IsExportNeeded](./get_isexportneeded/) property. 
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
