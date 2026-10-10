---
title: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine 方法"
linktitle: "get_MaxCharactersPerLine"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine 方法。获取或设置一个整数值，指定每行的最大字符数。默认值为 0，表示在 C++ 中没有限制。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


获取或设置一个整数值，指定每行的最大字符数。默认值为 0，这意味着无限制。

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## 示例



展示如何设置每行的最大字符数。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// 将每行允许的最大字符数设置为 30。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## 另见

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
