---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade 方法"
linktitle: "get_BackTintAndShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade 方法。获取或设置一个双精度值，用于在 C++ 中调亮或调暗背景颜色。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


获取或设置用于调亮或调暗背景颜色的 double 值。

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## 备注


此属性的允许值范围为 -1（最暗）到 1（最亮）。

零 (0) 为中性。

## 示例



展示如何为前景/背景形状颜色设置主题颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// 注意：不要在字体填充中使用 "BackThemeColor" 和 "BackTintAndShade"。
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## 另见

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
