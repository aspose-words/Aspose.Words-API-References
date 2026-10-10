---
title: "Aspose::Words::Saving::CssSavingArgs 类"
linktitle: "CssSavingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::CssSavingArgs 类。提供 CssSaving() 事件的数据。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


提供 [CssSaving()](../icsssavingcallback/csssaving/) 事件的数据。要了解更多，请访问 [保存文档](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class CssSavingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | 允许指定 CSS 信息将被保存到的流。 |
| [get_Document](./get_document/)() const | 获取当前正在保存的文档对象。 |
| [get_IsExportNeeded](./get_isexportneeded/)() const | 允许指定 CSS 是否导出到文件并嵌入到 HTML 文档中。默认是 **true**。当此属性为 **false** 时，CSS 信息将不会保存到 CSS 文件，也不会嵌入到 HTML 文档中。 |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | 指定 Aspose.Words 在保存 CSS 信息后是保持流打开还是关闭。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 用于 [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/) 的设置器。 |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | 允许指定 CSS 是否导出到文件并嵌入到 HTML 文档中。默认是 **true**。当此属性为 **false** 时，CSS 信息将不会保存到 CSS 文件，也不会嵌入到 HTML 文档中。 |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | 用于 [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/) 的设置器。 |
| static [Type](./type/)() |  |
## 备注


默认情况下，当 Aspose.Words 将文档保存为 HTML 时，它会将 CSS 信息内联保存（作为每个元素的 **style** 属性的值）。

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

要将 CSS 保存到流中，请使用 [CssStream](./get_cssstream/) 属性。

要抑制将 CSS 保存到文件并嵌入到 HTML 文档，请使用 [IsExportNeeded](./get_isexportneeded/) 属性。
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
