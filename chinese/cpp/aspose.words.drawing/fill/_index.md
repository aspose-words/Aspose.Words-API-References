---
title: "Aspose::Words::Drawing::Fill class"
linktitle: "Fill"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill 类。表示对象的填充格式。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.drawing/fill/
---
## Fill class


表示对象的填充格式。要了解更多信息，请访问 [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) 文档文章。

```cpp
class Fill : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | 获取或设置表示填充背景颜色的 Color 对象。 |
| [get_BackThemeColor](./get_backthemecolor/)() | 获取或设置表示填充背景颜色的 ThemeColor 对象。 |
| [get_BackTintAndShade](./get_backtintandshade/)() | 获取或设置用于调亮或调暗背景颜色的 double 值。 |
| [get_BaseForeColor](./get_baseforecolor/)() | 获取表示填充基础前景颜色（无任何修饰）的 Color 对象。 |
| [get_Color](./get_color/)() | 获取或设置表示填充前景颜色的 Color 对象。 |
| [get_FillType](./get_filltype/)() | 获取填充类型。 |
| [get_ForeColor](./get_forecolor/)() | 获取表示填充前景颜色的 Color 对象。 |
| [get_ForeThemeColor](./get_forethemecolor/)() | 获取或设置表示填充前景颜色的 ThemeColor 对象。 |
| [get_ForeTintAndShade](./get_foretintandshade/)() | 获取或设置用于调亮或调暗前景颜色的 double 值。 |
| [get_GradientAngle](./get_gradientangle/)() | 获取或设置渐变填充的角度。 |
| [get_GradientStops](./get_gradientstops/)() | 获取填充的 [GradientStop](../gradientstop/) 对象集合。 |
| [get_GradientStyle](./get_gradientstyle/)() | 获取用于填充的渐变样式 [GradientStyle](../gradientstyle/)。 |
| [get_GradientVariant](./get_gradientvariant/)() | 获取用于填充的渐变变体 [GradientVariant](../gradientvariant/)。 |
| [get_ImageBytes](./get_imagebytes/)() | 获取填充纹理或图案的原始字节。 |
| [get_Opacity](./get_opacity/)() | 获取或设置指定填充的不透明度程度，取值范围为 0.0（透明）到 1.0（不透明）。 |
| [get_Pattern](./get_pattern/)() | 获取用于填充的 [PatternType](../patterntype/)。 |
| [get_PresetTexture](./get_presettexture/)() | 获取用于填充的 [PresetTexture](../presettexture/)。 |
| [get_RotateWithObject](./get_rotatewithobject/)() | 获取填充是否随指定对象旋转。 |
| [get_TextureAlignment](./get_texturealignment/)() | 获取或设置平铺纹理填充的对齐方式。 |
| [get_Transparency](./get_transparency/)() | 获取或设置指定填充的透明度程度，取值范围为 0.0（不透明）到 1.0（透明）。 |
| [get_Visible](./get_visible/)() | 获取值，如果应用于此实例的格式可见，则为 **true**。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | 将指定填充设置为单色渐变。 |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | 使用指定颜色将指定填充设置为单色渐变。 |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | 将指定填充设置为图案。 |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | 将指定填充设置为图案。 |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | 将填充设置为预设纹理。 |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/) 的 setter。 |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | 用于设置 [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/) 的 setter。 |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | 用于设置 [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/) 的 setter。 |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Drawing::Fill::get_Color](./get_color/) 的 setter。 |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | 设置一个表示填充前景颜色的 Color 对象。 |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | 用于设置 [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/) 的 setter。 |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | 用于设置 [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/) 的 setter。 |
| [set_GradientAngle](./set_gradientangle/)(double) | 用于设置 [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/) 的 setter。 |
| [set_Opacity](./set_opacity/)(double) | 用于设置 [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/) 的 setter。 |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | 设置填充是否随指定对象旋转。 |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | 用于设置 [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/) 的 setter。 |
| [set_Transparency](./set_transparency/)(double) | 用于 [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/) 的设置器。 |
| [set_Visible](./set_visible/)(bool) | 如果应用于此实例的格式可见，则设置值为 **true**。 |
| [SetImage](./setimage/)(const System::String\&) | 将填充类型更改为单个图像。 |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | 将填充类型更改为单个图像。 |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | 将填充类型更改为单个图像。 |
| [Solid](./solid/)() | 将填充设置为统一颜色。 |
| [Solid](./solid/)(System::Drawing::Color) | 将填充设置为指定的统一颜色。 |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | 将指定的填充设置为双色渐变。 |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | 将指定的填充设置为双色渐变。 |
| static [Type](./type/)() |  |
## 备注


使用 [Fill](../shapebase/get_fill/) 或 [Fill](../../aspose.words/font/get_fill/) 属性来访问对象的填充属性。不要直接创建 [Fill](./) 类的实例。

## 示例



展示如何使用纯色填充形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 写入一些文本，然后用浮动形状覆盖它。
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// 使用 \"StrokeColor\" 属性设置形状轮廓的颜色。
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// 使用 \"FillColor\" 属性设置形状内部区域的颜色。
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// “Opacity” 属性决定颜色在 0-1 量表上的透明度，
// 其中 1 表示完全不透明，0 表示不可见。
// 形状填充默认是完全不透明的，因此我们看不到该形状上方的文本。
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// 将形状填充颜色的透明度设置为较低的值，以便我们能看到其下方的文本。
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
