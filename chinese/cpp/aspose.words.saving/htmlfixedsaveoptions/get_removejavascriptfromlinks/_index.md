---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks 方法"
linktitle: "get_RemoveJavaScriptFromLinks"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks 方法。指定是否从链接中移除 JavaScript。默认在 C++ 中为 false。"
type: docs
weight: 13500
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_removejavascriptfromlinks/
---
## HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks method


指定是否从链接中移除 JavaScript。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks() const
```


## 示例



展示如何从 html 固定文档的链接中移除 JavaScript。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```


展示如何从链接中移除 JavaScript。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"JavaScript in HREF.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_RemoveJavaScriptFromLinks(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
