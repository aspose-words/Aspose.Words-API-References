---
title: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor 方法"
linktitle: "get_DeleteCellColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor 方法。允许指定用于已删除单元格的颜色（Deletion）。默认值在 C++ 中为 Pink。"
type: docs
weight: 2500
url: /zh/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


允许指定用于已删除单元格的颜色 [Deletion](../../../aspose.words/revisiontype/)。默认值为 [Pink](../../revisioncolor/)。

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
```


## 示例



展示如何使用插入/删除单元格的修订颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## 另见

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
