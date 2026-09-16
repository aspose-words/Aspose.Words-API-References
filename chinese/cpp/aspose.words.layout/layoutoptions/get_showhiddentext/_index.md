---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText 方法"
linktitle: "get_ShowHiddenText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText 方法。获取或设置文档中隐藏文本是否被渲染的指示。默认在 C++ 中为 false。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


获取或设置指示文档中隐藏文本是否呈现的标志。默认值为 **false**。

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## 示例



展示如何在渲染的输出文档中隐藏文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入隐藏文本，然后指定是否希望在渲染的文档中省略它。
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## 另见

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
