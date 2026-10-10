---
title: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart 方法"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart 方法。获取或设置在连续节重新开始页码时计算页码的行为模式（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


获取或设置在连续节重新开始页码时计算页码的行为模式。

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## 示例



展示如何在连续节中控制页码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// 默认情况下，Aspose.Words 的行为匹配 Microsoft Word 2019。
// 如果需要旧的 Aspose.Words 行为（即 Microsoft Word 2016 的重复行为），请使用 'ContinuousSectionRestart.FromNewPageOnly'。
// 仅当章节开始的页面上在该章节之前没有其他内容时，页码才会重新开始，
// 因此，编号将在第二页起重置为 2。
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## 另见

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
