---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources 方法"
linktitle: "get_ExportFontResources"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources 方法。指定是否应将字体资源导出为 HTML、MHTML 或 EPUB。默认在 C++ 中为 false。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


指定是否应将字体资源导出到 HTML、MHTML 或 EPUB。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## 备注


导出字体资源可实现文档渲染的一致性，且不受用户环境中可用字体的影响。

如果将 [ExportFontResources](./) 设置为 **true**，主 HTML 文档将通过 CSS 3 **%@font-face** 规则引用每种字体，且字体将以独立文件形式输出。导出为 IDPF EPUB 或 MHTML 格式时，字体将与其他附属文件一起嵌入到相应的包中。

如果将 [ExportFontsAsBase64](../get_exportfontsasbase64/) 设置为 **true**，字体将不会保存为独立文件，而是以 Base64 编码嵌入到 **%@font-face** 规则中。

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
