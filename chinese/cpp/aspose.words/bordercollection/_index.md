---
title: "Aspose::Words::BorderCollection class"
linktitle: "BorderCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection 类。一个 Border 对象的集合。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/bordercollection/
---
## BorderCollection class


一个 [Border](../border/) 对象的集合。要了解更多信息，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 移除对象的所有边框。 |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | 比较边框集合。 |
| [get_Bottom](./get_bottom/)() | 获取底部边框。 |
| [get_Color](./get_color/)() | 获取或设置边框颜色。 |
| [get_Count](./get_count/)() | 获取集合中边框的数量。 |
| [get_DistanceFromText](./get_distancefromtext/)() | 获取或设置边框与文本之间的距离（单位：点）。 |
| [get_Horizontal](./get_horizontal/)() | 获取用于单元格或相邻段落之间的水平边框。 |
| [get_Left](./get_left/)() | 获取左侧边框。 |
| [get_LineStyle](./get_linestyle/)() | 获取或设置边框样式。 |
| [get_LineWidth](./get_linewidth/)() | 获取或设置以点为单位的边框宽度。 |
| [get_Right](./get_right/)() | 获取右侧边框。 |
| [get_Shadow](./get_shadow/)() | 获取或设置指示边框是否有阴影的值。 |
| [get_Top](./get_top/)() | 获取顶部边框。 |
| [get_Vertical](./get_vertical/)() | 获取用于单元格之间的垂直边框。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个可用于遍历集合中所有边框的枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | 通过边框类型检索一个 [Border](../border/) 对象。 |
| [idx_get](./idx_get/)(int32_t) | 通过索引检索一个 [Border](../border/) 对象。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于 [Aspose::Words::BorderCollection::get_Color](./get_color/) 的设置器。 |
| [set_DistanceFromText](./set_distancefromtext/)(double) | 用于 [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/) 的设置器。 |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | 用于 [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/) 的设置器。 |
| [set_LineWidth](./set_linewidth/)(double) | 用于 [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/) 的设置器。 |
| [set_Shadow](./set_shadow/)(bool) | 用于 [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/) 的设置器。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
