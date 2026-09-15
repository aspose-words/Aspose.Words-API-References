---
title: "Aspose::Words::Drawing::Fill فئة"
linktitle: "Fill"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Fill class. تمثل تنسيق التعبئة لكائن. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.drawing/fill/
---
## Fill class


يمثل تنسيق التعبئة لكائن. لمعرفة المزيد، زر مقالة الوثائق [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | يحصل أو يعيّن كائن Color الذي يمثل لون الخلفية للتعبئة. |
| [get_BackThemeColor](./get_backthemecolor/)() | يحصل أو يعيّن كائن ThemeColor الذي يمثل لون الخلفية للتعبئة. |
| [get_BackTintAndShade](./get_backtintandshade/)() | يحصل أو يعيّن قيمة double التي تُفتح أو تُغيم لون الخلفية. |
| [get_BaseForeColor](./get_baseforecolor/)() | يحصل على كائن Color الذي يمثل لون المقدمة الأساسي للتعبئة دون أي معدلات. |
| [get_Color](./get_color/)() | يحصل أو يعيّن كائن Color الذي يمثل لون المقدمة للتعبئة. |
| [get_FillType](./get_filltype/)() | يحصل على نوع التعبئة. |
| [get_ForeColor](./get_forecolor/)() | يحصل على كائن Color الذي يمثل لون المقدمة للتعبئة. |
| [get_ForeThemeColor](./get_forethemecolor/)() | يحصل أو يعيّن كائن ThemeColor الذي يمثل لون المقدمة للتعبئة. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | يحصل أو يعيّن قيمة double التي تُفتح أو تُغيم لون المقدمة. |
| [get_GradientAngle](./get_gradientangle/)() | يحصل أو يعيّن زاوية تعبئة التدرج. |
| [get_GradientStops](./get_gradientstops/)() | يحصل على مجموعة من كائنات [GradientStop](../gradientstop/) للتعبئة. |
| [get_GradientStyle](./get_gradientstyle/)() | يحصل على نمط التدرج [GradientStyle](../gradientstyle/) للتعبئة. |
| [get_GradientVariant](./get_gradientvariant/)() | يحصل على متغير التدرج [GradientVariant](../gradientvariant/) للتعبئة. |
| [get_ImageBytes](./get_imagebytes/)() | يحصل على البايتات الخام لنقش أو نمط التعبئة. |
| [get_Opacity](./get_opacity/)() | يحصل أو يعيّن درجة الشفافية للتعبئة المحددة كقيمة بين 0.0 (شفاف) و 1.0 (معتم). |
| [get_Pattern](./get_pattern/)() | يحصل على [PatternType](../patterntype/) للتعبئة. |
| [get_PresetTexture](./get_presettexture/)() | يحصل على [PresetTexture](../presettexture/) للتعبئة. |
| [get_RotateWithObject](./get_rotatewithobject/)() | يحصل على ما إذا كانت التعبئة تدور مع الكائن المحدد. |
| [get_TextureAlignment](./get_texturealignment/)() | يحصل أو يعيّن محاذاة تعبئة نسيج البلاط. |
| [get_Transparency](./get_transparency/)() | يحصل أو يعيّن درجة الشفافية للتعبئة المحددة كقيمة بين 0.0 (معتم) و 1.0 (شفاف). |
| [get_Visible](./get_visible/)() | يحصل على القيمة التي تكون **true** إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | يضبط التعبئة المحددة لتصبح تدرجًا بلون واحد. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | يضبط التعبئة المحددة لتصبح تدرجًا بلون واحد باستخدام اللون المحدد. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | يضبط التعبئة المحددة لتصبح نمطًا. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | يضبط التعبئة المحددة لتصبح نمطًا. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | يضبط التعبئة إلى نسيج مسبق الإعداد. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | المحدد لـ [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | المحدد لـ [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | المحدد لـ [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | المحدد لـ [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | يضبط كائن Color الذي يمثل لون المقدمة للتعبئة. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | المحدد لـ [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | المحدد لـ [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | المحدد لـ [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | المحدد لـ [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | يضبط ما إذا كانت التعبئة تدور مع الكائن المحدد. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | المحدد لـ [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | المحدد لـ [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | يضبط القيمة التي تكون **true** إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |
| [SetImage](./setimage/)(const System::String\&) | يغيّر نوع التعبئة إلى صورة واحدة. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | يغيّر نوع التعبئة إلى صورة واحدة. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | يغيّر نوع التعبئة إلى صورة واحدة. |
| [Solid](./solid/)() | يضبط التعبئة إلى لون موحد. |
| [Solid](./solid/)(System::Drawing::Color) | يضبط التعبئة إلى لون موحد محدد. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | يضبط التعبئة المحددة إلى تدرج لوني من لونين. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | يضبط التعبئة المحددة إلى تدرج لوني من لونين. |
| static [Type](./type/)() |  |
## ملاحظات


استخدم خاصية [Fill](../shapebase/get_fill/) أو [Fill](../../aspose.words/font/get_fill/) للوصول إلى خصائص التعبئة لكائن. لا تقوم بإنشاء مثيلات من الفئة [Fill](./) مباشرةً.

## أمثلة



يعرض كيفية تعبئة شكل بلون صلب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// اكتب بعض النص، ثم غطه بشكل عائم.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// استخدم خاصية "StrokeColor" لتعيين لون حدود الشكل.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// خاصية "Opacity" تحدد مدى شفافية اللون على مقياس من 0 إلى 1،
// حيث يكون 1 غير شفاف تمامًا، و0 غير مرئي.
// ملء الشكل بشكل افتراضي غير شفاف تمامًا، لذا لا يمكننا رؤية النص الذي يقع فوقه هذا الشكل.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// قم بتعيين شفافية لون ملء الشكل إلى قيمة أقل حتى نتمكن من رؤية النص تحته.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
