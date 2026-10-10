---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor 方法"
linktitle: "get_InsertCellColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor 方法。允许指定用于插入单元格 Insertion 的颜色。默认值是 Blue，在 C++ 中。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


允许指定用于插入单元格的颜色 [Insertion](../../../aspose.words/revisiontype/)。默认值是 [Blue](../../revisioncolor/)。

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
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
