---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName 方法"
linktitle: "get_FontFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName 方法。获取或设置在 C++ 中保存字体的文件名（不含路径）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


获取或设置字体将被保存到的文件名（不含路径）。

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## 备注


此属性允许您重新定义在导出为 HTML 时生成字体文件名的方式。

当事件触发时，此属性包含 Aspose.Words 生成的文件名。您可以更改此属性的值，以将字体保存到其他文件。请注意，文件名必须唯一。

Aspose.Words 在导出为 HTML 格式时会自动为每个嵌入的字体生成唯一的文件名。字体文件名的生成方式取决于您是将文档保存到文件还是流。

当将文档保存到文件时，生成的字体文件名类似于 *%<document base file name>.<original file name><optional suffix>.<extension>*。

当将文档保存到流时，生成的字体文件名类似于 *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*。

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## 另见

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
