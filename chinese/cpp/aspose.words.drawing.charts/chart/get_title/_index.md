---
title: "Aspose::Words::Drawing::Charts::Chart::get_Title 方法"
linktitle: "get_Title"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Charts::Chart::get_Title 方法。在 C++ 中提供对图表标题属性的访问。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing.charts/chart/get_title/
---
## Chart::get_Title method


提供对图表标题属性的访问。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> Aspose::Words::Drawing::Charts::Chart::get_Title()
```


## 示例



展示如何插入图表并设置标题。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入图表形状并获取其图表。
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// 使用 "Title" 属性为我们的图表添加标题，标题显示在图表区域的顶部中心。
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// 将 "Show" 属性设置为 "true"，使标题可见。
title->set_Show(true);

// 将 "Overlay" 属性设置为 "true"，通过允许标题被覆盖，为其他图表元素提供更多空间。
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## 另见

* Class [ChartTitle](../../charttitle/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
