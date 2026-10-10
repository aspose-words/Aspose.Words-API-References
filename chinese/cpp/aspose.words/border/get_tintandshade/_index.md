---
title: "Aspose::Words::Border::get_TintAndShade 方法"
linktitle: "get_TintAndShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border::get_TintAndShade 方法。获取或设置一个 double 值，以在 C++ 中调亮或调暗颜色。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


获取或设置用于使颜色变亮或变暗的双精度值。

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## 备注


此属性的允许值范围为 -1（最暗）到 1（最亮）。零 (0) 为中性。

## 示例



展示如何插入带有顶部边框的段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// 仅在设置了 LineWidth 或 LineStyle 时才设置 ThemeColor。
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## 另见

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
