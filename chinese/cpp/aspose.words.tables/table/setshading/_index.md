---
title: "Aspose::Words::Tables::Table::SetShading method"
linktitle: "SetShading"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::SetShading 方法。将在 C++ 中对整个表设置指定的阴影值。"
type: docs
weight: 70000
url: /zh/cpp/aspose.words.tables/table/setshading/
---
## Table::SetShading method


将整个表格的阴影设置为指定的值。

```cpp
void Aspose::Words::Tables::Table::SetShading(Aspose::Words::TextureIndex texture, System::Drawing::Color foregroundColor, System::Drawing::Color backgroundColor)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 纹理 | Aspose::Words::TextureIndex | 要应用的纹理。 |
| 前景颜色 | System::Drawing::Color | 纹理的颜色。 |
| 背景颜色 | System::Drawing::Color | 背景填充的颜色。 |

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

* Enum [TextureIndex](../../../aspose.words/textureindex/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
