---
title: "Aspose::Words::Layout::ContinuousSectionRestart 枚举"
linktitle: "ContinuousSectionRestart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::ContinuousSectionRestart 枚举。表示在 C++ 中连续节重新开始页码时计算页码的不同行为。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


表示在连续节中重新开始页码时计算页码的不同行为。

```cpp
enum class ContinuousSectionRestart
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 始终 | 0 | 页码始终重新开始，无论内容流如何。 |
| FromNewPageOnly | 1 | 仅当章节开始的页面上在该章节之前没有其他内容时，页码才会重新开始。 |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
