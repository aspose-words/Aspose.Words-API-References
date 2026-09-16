---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontStream 方法"
linktitle: "get_FontStream"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontStream 方法。允许在 C++ 中指定保存字体的流。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.saving/fontsavingargs/get_fontstream/
---
## FontSavingArgs::get_FontStream method


允许指定字体将被保存到的流。

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::FontSavingArgs::get_FontStream() const
```

## 备注


此属性允许在 HTML 导出期间将字体保存到流而不是文件。

默认值为 **null**。当此属性为 **null** 时，字体将保存到在 [FontFileName](../get_fontfilename/) 属性中指定的文件。

## 另见

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
