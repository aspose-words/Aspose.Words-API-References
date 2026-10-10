---
title: "Aspose::Words::Border::get_ThemeColor 方法"
linktitle: "get_ThemeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border::get_ThemeColor 方法。获取或设置与此 Border 对象关联的已应用配色方案中的主题颜色（C++）。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


获取或设置与此 [Border](../) 对象关联的已应用配色方案中的主题颜色。

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
