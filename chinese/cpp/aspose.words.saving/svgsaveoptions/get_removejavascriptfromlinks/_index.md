---
title: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks 方法"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks 方法。指定是否从链接中移除 JavaScript。默认值为 false。如果启用此选项，所有包含 JavaScript 的链接将在 C++ 中被替换为 \\\"javascript:void(0)\\\"。"
type: docs
weight: 4750
url: /zh/cpp/aspose.words.saving/svgsaveoptions/get_removejavascriptfromlinks/
---
## SvgSaveOptions::get_RemoveJavaScriptFromLinks method


指定是否从链接中移除 JavaScript。默认值为 **false**。如果启用此选项，所有包含 JavaScript 的链接将被替换为 "javascript:void(0)"。

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## 示例



展示如何从链接（svg）中移除 JavaScript。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

## 另见

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
