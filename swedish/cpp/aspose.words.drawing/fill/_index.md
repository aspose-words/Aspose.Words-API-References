---
title: "Aspose::Words::Drawing::Fill class"
linktitle: "Fill"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Fill class. Representerar fyllningsformatering för ett objekt. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.drawing/fill/
---
## Fill class


Representerar fyllningsformatering för ett objekt. För att lära dig mer, besök dokumentationsartikeln [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Hämtar eller anger ett Color-objekt som representerar bakgrundsfärgen för fyllningen. |
| [get_BackThemeColor](./get_backthemecolor/)() | Hämtar eller anger ett ThemeColor-objekt som representerar bakgrundsfärgen för fyllningen. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar bakgrundsfärgen. |
| [get_BaseForeColor](./get_baseforecolor/)() | Hämtar ett Color-objekt som representerar basförgrundsfärgen för fyllningen utan några modifierare. |
| [get_Color](./get_color/)() | Hämtar eller anger ett Color-objekt som representerar förgrundsfärgen för fyllningen. |
| [get_FillType](./get_filltype/)() | Hämtar en fyllningstyp. |
| [get_ForeColor](./get_forecolor/)() | Hämtar ett Color-objekt som representerar förgrundsfärgen för fyllningen. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Hämtar eller anger ett ThemeColor-objekt som representerar förgrundsfärgen för fyllningen. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar förgrundsfärgen. |
| [get_GradientAngle](./get_gradientangle/)() | Hämtar eller anger vinkeln på gradientfyllningen. |
| [get_GradientStops](./get_gradientstops/)() | Hämtar en samling av [GradientStop](../gradientstop/) objekt för fyllningen. |
| [get_GradientStyle](./get_gradientstyle/)() | Hämtar gradientstilen [GradientStyle](../gradientstyle/) för fyllningen. |
| [get_GradientVariant](./get_gradientvariant/)() | Hämtar gradientvarianten [GradientVariant](../gradientvariant/) för fyllningen. |
| [get_ImageBytes](./get_imagebytes/)() | Hämtar de råa bytena för fyllningstexturen eller mönstret. |
| [get_Opacity](./get_opacity/)() | Hämtar eller anger opacitetsgraden för den angivna fyllningen som ett värde mellan 0.0 (clear) och 1.0 (opaque). |
| [get_Pattern](./get_pattern/)() | Hämtar en [PatternType](../patterntype/) för fyllningen. |
| [get_PresetTexture](./get_presettexture/)() | Hämtar en [PresetTexture](../presettexture/) för fyllningen. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Hämtar om fyllningen roterar med det angivna objektet. |
| [get_TextureAlignment](./get_texturealignment/)() | Hämtar eller anger justeringen för kakeltexturfyllning. |
| [get_Transparency](./get_transparency/)() | Hämtar eller anger transparensgraden för den angivna fyllningen som ett värde mellan 0.0 (opaque) och 1.0 (clear). |
| [get_Visible](./get_visible/)() | Hämtar värdet som är **true** om formateringen som tillämpas på detta objekt är synlig. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Ställer in den angivna fyllningen till en enfärgsgradient. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Ställer in den angivna fyllningen till en enfärgsgradient med den angivna färgen. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Ställer in den angivna fyllningen till ett mönster. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Ställer in den angivna fyllningen till ett mönster. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Ställer in fyllningen till en förinställd textur. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Sättare för [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Sättare för [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Inställare för [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Inställare för [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Sätter ett Color-objekt som representerar förgrundsfärgen för fyllningen. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Inställare för [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Inställare för [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Inställare för [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Inställare för [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Anger om fyllningen roterar med det angivna objektet. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Inställare för [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Inställare för [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Sätter värdet till **true** om formateringen som tillämpats på detta objekt är synlig. |
| [SetImage](./setimage/)(const System::String\&) | Ändrar fyllningstypen till en enda bild. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Ändrar fyllningstypen till en enda bild. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Ändrar fyllningstypen till en enda bild. |
| [Solid](./solid/)() | Ställer in fyllningen till en enhetlig färg. |
| [Solid](./solid/)(System::Drawing::Color) | Ställer in fyllningen till en specificerad enhetlig färg. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Ställer in den specificerade fyllningen till en tvåfärgsgradient. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Ställer in den specificerade fyllningen till en tvåfärgsgradient. |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [Fill](../shapebase/get_fill/) eller [Fill](../../aspose.words/font/get_fill/) för att komma åt fyllningsegenskaper för ett objekt. Du skapar inte instanser av klassen [Fill](./) direkt.

## Exempel



Visar hur man fyller en form med en solid färg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skriv lite text och täck sedan den med en flytande form.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Använd egenskapen "StrokeColor" för att ange färgen på formens kontur.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Använd egenskapen "FillColor" för att ange färgen på formens inneryta.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// Egenskapen "Opacity" bestämmer hur genomskinlig färgen är på en skala från 0 till 1,
// där 1 är helt ogenomskinlig och 0 är osynlig.
// Formens fyllning är som standard helt ogenomskinlig, så vi kan inte se texten som den ligger ovanpå.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Sätt formens fyllningsfärgs opacitet till ett lägre värde så att vi kan se texten under den.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
