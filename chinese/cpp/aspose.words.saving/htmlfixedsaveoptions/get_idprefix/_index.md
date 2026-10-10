---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix 方法"
linktitle: "get_IdPrefix"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix 方法。指定在输出文档中所有生成的元素 ID 前面添加的前缀。默认值为 null，在 C++ 中不添加前缀。"
type: docs
weight: 10500
url: /zh/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


指定一个前缀，该前缀会预先添加到输出文档中所有生成的元素 ID 前。默认值为 null，且不添加前缀。

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## 示例



展示如何添加一个前缀，以便在所有生成的元素 ID 前面添加。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## 另见

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
