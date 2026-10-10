---
title: "Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars 方法"
linktitle: "get_ShowRevisionBars"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars 方法。允许指定是否在包含修订内容的行旁渲染修订条。默认值在 C++ 中为 true。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.layout/revisionoptions/get_showrevisionbars/
---
## RevisionOptions::get_ShowRevisionBars method


允许指定是否应在包含修订内容的行附近渲染修订栏。默认值是 **true**。

```cpp
bool Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars() const
```


## 示例



展示如何更改渲染的输出文档中修订的外观。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入修订，然后将所有修订的颜色更改为绿色。
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// 移除出现在每条修订行左侧的条形标记。
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## 另见

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
