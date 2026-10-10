---
title: "Aspose::Words::Shading 类"
linktitle: "Shading"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Shading 类。包含对象的阴影属性。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 60000
url: /zh/cpp/aspose.words/shading/
---
## Shading class


包含对象的阴影属性。要了解更多，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 从对象中移除阴影。 |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | 确定指定的 [Shading](./) 在数值上是否等于当前的 [Shading](./)。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | 获取或设置应用于 [Shading](./) 对象背景的颜色。 |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | 获取或设置与此 [Shading](./) 对象关联的已应用配色方案中的背景图案主题颜色。 |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | 获取或设置用于调亮或调暗背景主题颜色的 double 值。 |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | 获取或设置应用于 [Shading](./) 对象前景的颜色。 |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | 获取或设置与此 [Shading](./) 对象关联的已应用配色方案中的前景图案主题颜色。 |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | 获取或设置用于调亮或调暗前景主题颜色的 double 值。 |
| [get_Texture](./get_texture/)() | 获取或设置阴影纹理。 |
| [GetHashCode](./gethashcode/)() const override | 作为此类型的哈希函数。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/) 的 setter。 |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | 用于设置 [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/) 的 setter。 |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | 用于设置 [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/) 的 setter。 |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/) 的 setter。 |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | 用于设置 [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/) 的 setter。 |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | 用于设置 [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/) 的 setter。 |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | 用于设置 [Aspose::Words::Shading::get_Texture](./get_texture/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何在构建表格时应用边框和阴影颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 开始一个表格并为其边框设置默认颜色/粗细。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// 创建一行，其中两个单元格具有不同的背景颜色。
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// 重置单元格格式以禁用背景颜色
// 为构建器创建的所有新单元格设置自定义边框粗细，
// 然后构建第二行。
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


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

## 另见

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
