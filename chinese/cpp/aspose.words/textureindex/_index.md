---
title: "Aspose::Words::TextureIndex 枚举"
linktitle: "TextureIndex"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextureIndex 枚举。指定 C++ 中的阴影纹理。"
type: docs
weight: 125000
url: /zh/cpp/aspose.words/textureindex/
---
## TextureIndex enum


指定阴影纹理。

```cpp
enum class TextureIndex
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Texture10Percent | 3 |  |
| Texture12Pt5Percent | 37 |  |
| Texture15Percent | 38 |  |
| Texture17Pt5Percent | 39 |  |
| Texture20Percent | 4 |  |
| Texture22Pt5Percent | 40 |  |
| Texture25Percent | 5 |  |
| Texture27Pt5Percent | 41 |  |
| Texture2Pt5Percent | 35 |  |
| Texture30Percent | 6 |  |
| Texture32Pt5Percent | 42 |  |
| Texture35Percent | 43 |  |
| Texture37Pt5Percent | 44 |  |
| Texture40Percent | 7 |  |
| Texture42Pt5Percent | 45 |  |
| Texture45Percent | 46 |  |
| Texture47Pt5Percent | 47 |  |
| Texture50Percent | 8 |  |
| Texture52Pt5Percent | 48 |  |
| Texture55Percent | 49 |  |
| Texture57Pt5Percent | 50 |  |
| Texture5Percent | 2 |  |
| Texture60Percent | 9 |  |
| Texture62Pt5Percent | 51 |  |
| 纹理65百分比 | 52 |  |
| 纹理67.5百分比 | 53 |  |
| 纹理70百分比 | 10 |  |
| 纹理72.5百分比 | 54 |  |
| 纹理75百分比 | 11 |  |
| 纹理77.5百分比 | 55 |  |
| 纹理7.5百分比 | 36 |  |
| 纹理80百分比 | 12 |  |
| 纹理82.5百分比 | 56 |  |
| 纹理85百分比 | 57 |  |
| 纹理87.5百分比 | 58 |  |
| 纹理90百分比 | 13 |  |
| 纹理92.5百分比 | 59 |  |
| 纹理95百分比 | 60 |  |
| 纹理97.5百分比 | 61 |  |
| 纹理交叉 | 24 |  |
| 纹理深色交叉 | 18 |  |
| 纹理深色对角交叉 | 19 |  |
| 纹理深色对角向下 | 16 |  |
| 纹理深色对角向上 | 17 |  |
| 纹理深色水平 | 14 |  |
| 纹理深色垂直 | 15 |  |
| 纹理对角交叉 | 25 |  |
| 纹理对角向下 | 22 |  |
| 纹理对角向上 | 23 |  |
| TextureHorizontal | 20 |  |
| TextureNone | 0 |  |
| TextureSolid | 1 |  |
| TextureVertical | 21 |  |
| TextureNil | 65535 | 指定当前阴影区域不应使用任何图案（即图案应完全填充为背景颜色）。 |


## 示例



展示如何使用边框和阴影装饰文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
