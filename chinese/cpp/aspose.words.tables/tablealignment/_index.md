---
title: "Aspose::Words::Tables::TableAlignment 枚举"
linktitle: "TableAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::TableAlignment 枚举。指定 C++ 中内联表格的对齐方式。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


指定内联表格的对齐方式。

```cpp
enum class TableAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 左 | 0 | 表格左对齐。 |
| 居中 | 1 | 表格已居中。 |
| 右 | 2 | 表格已右对齐。 |


## 示例



展示如何对表格应用外框边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 将表格对齐到页面中心。
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// 清除表格中所有现有的边框和阴影。
table->ClearBorders();
table->ClearShading();

// 为表格的外框添加绿色边框。
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// 用浅绿色实色填充单元格。
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## 另见

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
