---
title: "Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons 方法"
linktitle: "get_ShowInBalloons"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons 方法。允许指定是否在气泡中呈现修订。默认值在 C++ 中为 None。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.layout/revisionoptions/get_showinballoons/
---
## RevisionOptions::get_ShowInBalloons method


允许指定是否在气泡中呈现修订。默认值为 [None](../../showinballoons/)。

```cpp
Aspose::Words::Layout::ShowInBalloons Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons() const
```


## 示例



展示如何在气泡中显示修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// 默认情况下，作为修订的文本会使用不同的颜色，以便与其他非修订文本区分。
// 设置修订选项，以在页面右侧边距的气泡中显示每个修订的更多详细信息。
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::FormatAndDelete);
doc->Save(get_ArtifactsDir() + u"Revision.ShowRevisionBalloons.pdf");
```


展示如何修改修订的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// 获取控制修订外观的 RevisionOptions 对象。
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// 以绿色和斜体呈现插入修订。
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// 以红色和粗体呈现删除修订。
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// 相同的文本将在移动修订中出现两次：
// 一次在出发点，另一次在到达目的地。
// 在移动前的修订处将文本渲染为黄色并带双删除线
// 并在移动后的修订处渲染为双下划线蓝色。
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// 以深红色和粗体呈现格式修订。
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// 在页面左侧紧邻受修订影响的行处放置一条粗暗蓝色条。
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// 显示修订标记和原始文本。
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// 使移动、删除、格式修订和批注以绿色气泡显示
// 在页面右侧。
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// 这些功能仅适用于 .pdf 或 .jpg 等格式。
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## 另见

* Enum [ShowInBalloons](../../showinballoons/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
