---
title: "Aspose::Words::Font::get_AutoColor 方法"
linktitle: "get_AutoColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_AutoColor 方法。返回用于 ''auto color'' 的文本当前计算颜色（黑色或白色）。如果颜色不是 ''auto''，则在 C++ 中返回 Color。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


返回用于 'auto color' 的文本当前计算颜色（黑色或白色）。如果颜色不是 'auto'，则返回 [Color](../get_color/)。

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## 备注


当文本具有“自动颜色”时，文本的实际颜色会自动计算，以确保在背景颜色下可读。随着背景颜色的变化，MS Word 中的文本颜色会自动切换为黑色或白色，以最大化可读性。

## 示例



展示如何通过根据背景亮度自动选择文本颜色来提升可读性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果 run 的 Font 对象未指定文本颜色，它将自动使用默认颜色。
// 根据背景颜色的颜色选择黑色或白色。
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// 文本的默认颜色是黑色。如果背景颜色较暗，黑色文本将难以看清。
// 为了解决此问题，AutoColor 属性将以白色显示此文本。
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// 如果我们将背景更改为浅色，黑色将更
// 适合作为文本颜色，而不是白色，这样自动颜色将以黑色显示。
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
