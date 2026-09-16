---
title: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded 方法"
linktitle: "get_IsSubsettingNeeded"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded 方法。允许指定在 C++ 中导出为字体资源之前是否对当前字体进行子集化。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


允许指定在导出为字体资源之前是否对当前字体进行子集化。

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## 备注


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

默认情况下，Aspose.Words 通过比较原始字体文件大小与在 [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/) 中指定的大小来决定是否执行子集化。您可以通过设置 [IsSubsettingNeeded](./) 属性来覆盖单个字体的此行为。
## 另见

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
