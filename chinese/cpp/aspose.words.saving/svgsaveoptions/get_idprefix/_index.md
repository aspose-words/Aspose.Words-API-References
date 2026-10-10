---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix 方法"
linktitle: "get_IdPrefix"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix 方法。指定在输出文档中所有生成的元素 ID 前面添加的前缀。默认值在 C++ 中为 null，且不添加前缀。"
type: docs
weight: 4250
url: /zh/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


指定一个前缀，该前缀会预先添加到输出文档中所有生成的元素 ID 前。默认值为 null，且不添加前缀。

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## 示例



展示如何添加一个前缀，以在所有生成的元素 ID 前面添加（svg）。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## 另见

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
