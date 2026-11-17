---
title: Aspose::Words::Saving::FontSavingArgs class
linktitle: FontSavingArgs
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::FontSavingArgs class. Provides data for the FontSaving() event. To learn more, visit the  documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Provides data for the [FontSaving()](../ifontsavingcallback/fontsaving/) event. To learn more, visit the [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) documentation article.

```cpp
class FontSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Bold](./get_bold/)() const | Indicates whether the current font is bold. |
| [get_Document](./get_document/)() const | Gets the document object that is being saved. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Indicates the current font family name. |
| [get_FontFileName](./get_fontfilename/)() const | Gets or sets the file name (without path) where the font will be saved to. |
| [get_FontStream](./get_fontstream/)() const | Allows to specify the stream where the font will be saved to. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Allows to specify whether the current font will be exported as a font resource. Default is **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [get_Italic](./get_italic/)() const | Indicates whether the current font is italic. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [get_OriginalFileName](./get_originalfilename/)() const | Gets the original font file name with an extension. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Gets the original font file size. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Allows to specify whether the current font will be exported as a font resource. Default is **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Remarks


When Aspose.Words saves a document to HTML or related formats and [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) is set to **true**, it saves each font subject for export into a separate file.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [IsExportNeeded](./get_isexportneeded/) property.

To save fonts into streams instead of files, use the [FontStream](./get_fontstream/) property. 
## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
