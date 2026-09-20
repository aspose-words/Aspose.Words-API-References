---
title: "Aspose::Words::Drawing::PresetTexture 枚举"
linktitle: "PresetTexture"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::PresetTexture 枚举。指定在 C++ 中用于填充形状的纹理。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words.drawing/presettexture/
---
## PresetTexture enum


指定用于填充形状的纹理。

```cpp
enum class PresetTexture
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | -1 | 无纹理。 |
| BlueTissuePaper | 1 | 蓝色纸巾纹理。 |
| Bouquet | 2 | 花束纹理。 |
| BrownMarble | 3 | 棕色大理石纹理。 |
| Canvas | 4 | 帆布纹理。 |
| Cork | 5 | 软木纹理。 |
| Denim | 6 | 牛仔布纹理。 |
| FishFossil | 7 | 鱼化石纹理。 |
| Granite | 8 | 花岗岩纹理。 |
| 绿色大理石 | 9 | 绿色大理石纹理。 |
| 中等木材 | 10 | 中等木材纹理。 |
| 新闻纸 | 11 | 新闻纸纹理。 |
| 橡木 | 12 | 橡木纹理。 |
| 纸袋 | 13 | 纸袋纹理。 |
| 纸莎草 | 14 | 纸莎草纹理。 |
| 羊皮纸 | 15 | 羊皮纸纹理。 |
| 粉红纸巾 | 16 | 粉红纸巾纹理。 |
| 紫色网格 | 17 | 紫色网格纹理。 |
| 再生纸 | 18 | 再生纸纹理。 |
| 沙子 | 19 | 沙子纹理。 |
| 文具 | 20 | 文具纹理。 |
| 胡桃木 | 21 | 核桃纹理。 |
| 水滴 | 22 | 水滴纹理。 |
| 白色大理石 | 23 | 白色大理石纹理。 |
| 编织垫 | 24 | 编织垫纹理。 |


## 示例



展示如何设置标记格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// 删除默认生成的系列。
chart->get_Series()->Clear();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<double>({0.7, 1.8, 2.6, 3.9}), System::MakeArray<double>({2.7, 3.2, 0.8, 1.7}));

// 设置标记格式。
series->get_Marker()->set_Size(40);
series->get_Marker()->set_Symbol(Aspose::Words::Drawing::Charts::MarkerSymbol::Square);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(0)->get_Marker()->get_Format()->get_Stroke()->set_BackColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::WaterDroplets);
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(1)->get_Marker()->get_Format()->get_Stroke()->set_Visible(false);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::GreenMarble);
dataPoints->idx_get(2)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Oak);
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Marker()->get_Format()->get_Stroke()->set_Transparency(0.5);

doc->Save(get_ArtifactsDir() + u"Charts.MarkerFormatting.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
