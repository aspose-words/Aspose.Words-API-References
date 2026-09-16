---
title: "Aspose::Words::Saving::FontSavingArgs 类"
linktitle: "FontSavingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::FontSavingArgs 类。提供 FontSaving() 事件的数据。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


提供 [FontSaving()](../ifontsavingcallback/fontsaving/) 事件的数据。要了解更多，请访问 [保存文档](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class FontSavingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Bold](./get_bold/)() const | 指示当前字体是否为粗体。 |
| [get_Document](./get_document/)() const | 获取正在保存的文档对象。 |
| [get_FontFamilyName](./get_fontfamilyname/)() const | 指示当前字体族名称。 |
| [get_FontFileName](./get_fontfilename/)() const | 获取或设置字体将被保存到的文件名（不含路径）。 |
| [get_FontStream](./get_fontstream/)() const | 允许指定字体将被保存到的流。 |
| [get_IsExportNeeded](./get_isexportneeded/)() const | 允许指定当前字体是否将导出为字体资源。默认值为 **true**。 |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | 允许指定在导出为字体资源之前是否对当前字体进行子集化。 |
| [get_Italic](./get_italic/)() const | 指示当前字体是否为斜体。 |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | 指定 Aspose.Words 在保存字体后是保持流打开还是关闭。 |
| [get_OriginalFileName](./get_originalfilename/)() const | 获取带扩展名的原始字体文件名。 |
| [get_OriginalFileSize](./get_originalfilesize/)() const | 获取原始字体文件大小。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/) 的 setter。 |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 用于设置 [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/) 的 setter。 |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | 允许指定当前字体是否将导出为字体资源。默认值为 **true**。 |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | 用于设置 [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/) 的 setter。 |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | 用于设置 [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


当 Aspose.Words 将文档保存为 HTML 或相关格式且 [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) 设置为 **true** 时，它会将每个字体资源导出为单独的文件。

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

要决定是否保存特定的字体资源，请使用 [IsExportNeeded](./get_isexportneeded/) 属性。

要将字体保存到流而不是文件，请使用 [FontStream](./get_fontstream/) 属性。
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
