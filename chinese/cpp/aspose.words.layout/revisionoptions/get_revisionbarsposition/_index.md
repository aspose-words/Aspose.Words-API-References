---
title: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition 方法"
linktitle: "get_RevisionBarsPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition 方法。获取或设置修订栏的渲染位置。默认在 C++ 中为 Outside。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


获取或设置修订栏的渲染位置。默认值为 [Outside](../../../aspose.words.drawing/horizontalalignment/)。

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
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

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
