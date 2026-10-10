---
title: "Aspose::Words::Font::get_TintAndShade 方法"
linktitle: "get_TintAndShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_TintAndShade 方法。获取或设置一个 double 值，以在 C++ 中调亮或调暗颜色。"
type: docs
weight: 54000
url: /zh/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


获取或设置用于使颜色变亮或变暗的双精度值。

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## 备注


此属性的允许值范围为 -1（最暗）到 1（最亮）。

零 (0) 为中性。

## 示例



展示如何创建和使用主题样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// 创建带有主题字体属性的样式。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
