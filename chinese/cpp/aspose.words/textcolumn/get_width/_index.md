---
title: "Aspose::Words::TextColumn::get_Width 方法"
linktitle: "get_Width"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextColumn::get_Width 方法。获取或设置文本列的宽度（单位：点），在 C++ 中。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/textcolumn/get_width/
---
## TextColumn::get_Width method


获取或设置文本列的宽度（单位为点）。

```cpp
double Aspose::Words::TextColumn::get_Width()
```


## 示例



展示如何创建间距不均匀的列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// 确定用于排列列的可用空间量。
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// 将第一列设为窄列。
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// 将第二列设为占据页面页边距内剩余的全部空间。
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## 另见

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
