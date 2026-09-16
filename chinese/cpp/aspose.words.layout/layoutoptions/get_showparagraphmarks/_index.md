---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks 方法"
linktitle: "get_ShowParagraphMarks"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks 方法。获取或设置是否渲染段落标记的指示。默认在 C++ 中为 false。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


获取或设置指示段落标记是否呈现的标志。默认值为 **false**。

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## 示例



展示如何在渲染的输出文档中显示段落标记。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加一些段落，然后启用段落标记以显示段落末尾
// 在渲染文档时使用段落符号 (¶)。
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## 另见

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
