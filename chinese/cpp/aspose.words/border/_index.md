---
title: "Aspose::Words::Border class"
linktitle: "边框"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border 类。表示对象的边框。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/border/
---
## Border class


表示对象的边框。欲了解更多，请访问[文档编程指南](https://docs.aspose.com/words/cpp/programming-with-documents/)文档文章。

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 将边框属性重置为默认值。 |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | 确定指定的边框在数值上是否等于当前边框。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_Color](./get_color/)() | 获取或设置边框颜色。 |
| [get_DistanceFromText](./get_distancefromtext/)() | 获取或设置边框距离文本或页面边缘的距离（单位：点）。 |
| [get_IsVisible](./get_isvisible/)() | 如果 [LineStyle](./get_linestyle/) 不是 [None](../linestyle/)，则返回 **true**。 |
| [get_LineStyle](./get_linestyle/)() | 获取或设置边框样式。 |
| [get_LineWidth](./get_linewidth/)() | 获取或设置以点为单位的边框宽度。 |
| [get_Shadow](./get_shadow/)() | 获取或设置指示边框是否有阴影的值。 |
| [get_ThemeColor](./get_themecolor/)() | 获取或设置与此 [Border](./) 对象关联的已应用配色方案中的主题颜色。 |
| [get_TintAndShade](./get_tintandshade/)() | 获取或设置用于使颜色变亮或变暗的双精度值。 |
| [GetHashCode](./gethashcode/)() const override | 作为此类型的哈希函数。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Border::get_Color](./get_color/) 的方法。 |
| [set_DistanceFromText](./set_distancefromtext/)(double) | 用于设置 [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/) 的方法。 |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | 用于设置 [Aspose::Words::Border::get_LineStyle](./get_linestyle/) 的方法。 |
| [set_LineWidth](./set_linewidth/)(double) | 用于设置 [Aspose::Words::Border::get_LineWidth](./get_linewidth/) 的方法。 |
| [set_Shadow](./set_shadow/)(bool) | 用于设置 [Aspose::Words::Border::get_Shadow](./get_shadow/) 的方法。 |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | 用于设置 [Aspose::Words::Border::get_ThemeColor](./get_themecolor/) 的方法。 |
| [set_TintAndShade](./set_tintandshade/)(double) | 用于设置 [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/) 的方法。 |
| static [Type](./type/)() |  |
## 备注


边框可以应用于各种文档元素，包括段落、段落内的文本运行或表格单元格。

## 示例



展示如何在文档中插入被边框包围的字符串。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


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

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
