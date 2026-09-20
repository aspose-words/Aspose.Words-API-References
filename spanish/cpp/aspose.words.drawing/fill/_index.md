---
title: "Clase Aspose::Words::Drawing::Fill"
linktitle: "Fill"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Fill. Representa el formato de relleno para un objeto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.drawing/fill/
---
## Fill class


Representa el formato de relleno para un objeto. Para obtener más información, visite el artículo de documentación [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/).

```cpp
class Fill : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Obtiene o establece un objeto Color que representa el color de fondo del relleno. |
| [get_BackThemeColor](./get_backthemecolor/)() | Obtiene o establece un objeto ThemeColor que representa el color de fondo del relleno. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Obtiene o establece un valor double que aclara o oscurece el color de fondo. |
| [get_BaseForeColor](./get_baseforecolor/)() | Obtiene un objeto Color que representa el color de primer plano base del relleno sin ningún modificador. |
| [get_Color](./get_color/)() | Obtiene o establece un objeto Color que representa el color de primer plano del relleno. |
| [get_FillType](./get_filltype/)() | Obtiene un tipo de relleno. |
| [get_ForeColor](./get_forecolor/)() | Obtiene un objeto Color que representa el color de primer plano del relleno. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Obtiene o establece un objeto ThemeColor que representa el color de primer plano del relleno. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Obtiene o establece un valor double que aclara o oscurece el color de primer plano. |
| [get_GradientAngle](./get_gradientangle/)() | Obtiene o establece el ángulo del relleno degradado. |
| [get_GradientStops](./get_gradientstops/)() | Obtiene una colección de objetos [GradientStop](../gradientstop/) para el relleno. |
| [get_GradientStyle](./get_gradientstyle/)() | Obtiene el estilo de degradado [GradientStyle](../gradientstyle/) para el relleno. |
| [get_GradientVariant](./get_gradientvariant/)() | Obtiene la variante de degradado [GradientVariant](../gradientvariant/) para el relleno. |
| [get_ImageBytes](./get_imagebytes/)() | Obtiene los bytes sin procesar de la textura o patrón de relleno. |
| [get_Opacity](./get_opacity/)() | Obtiene o establece el grado de opacidad del relleno especificado como un valor entre 0.0 (transparente) y 1.0 (opaco). |
| [get_Pattern](./get_pattern/)() | Obtiene un [PatternType](../patterntype/) para el relleno. |
| [get_PresetTexture](./get_presettexture/)() | Obtiene una [PresetTexture](../presettexture/) para el relleno. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Obtiene si el relleno rota con el objeto especificado. |
| [get_TextureAlignment](./get_texturealignment/)() | Obtiene o establece la alineación para el relleno de textura de mosaico. |
| [get_Transparency](./get_transparency/)() | Obtiene o establece el grado de transparencia del relleno especificado como un valor entre 0.0 (opaco) y 1.0 (transparente). |
| [get_Visible](./get_visible/)() | Obtiene un valor que es **true** si el formato aplicado a esta instancia es visible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Establece el relleno especificado a un degradado de un solo color. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Establece el relleno especificado a un degradado de un solo color usando el color especificado. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Establece el relleno especificado a un patrón. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Establece el relleno especificado a un patrón. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Establece el relleno a una textura predefinida. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Establecedor de [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Establecedor de [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Establece un objeto Color que representa el color de primer plano del relleno. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Establecedor de [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Establecedor de [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Establecedor de [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Establecedor de [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Establece si el relleno rota con el objeto especificado. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Establecedor de [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Establecedor de [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Establece el valor que es **true** si el formato aplicado a esta instancia es visible. |
| [SetImage](./setimage/)(const System::String\&) | Cambia el tipo de relleno a una sola imagen. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Cambia el tipo de relleno a una sola imagen. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Cambia el tipo de relleno a una sola imagen. |
| [Solid](./solid/)() | Establece el relleno a un color uniforme. |
| [Solid](./solid/)(System::Drawing::Color) | Establece el relleno a un color uniforme especificado. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Establece el relleno especificado a un degradado de dos colores. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Establece el relleno especificado a un degradado de dos colores. |
| static [Type](./type/)() |  |
## Observaciones


Utiliza la propiedad [Fill](../shapebase/get_fill/) o [Fill](../../aspose.words/font/get_fill/) para acceder a las propiedades de relleno de un objeto. No creas instancias de la clase [Fill](./) directamente.

## Ejemplos



Muestra cómo rellenar una forma con un color sólido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Escribe algún texto y luego cúbrelo con una forma flotante.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Utiliza la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Utiliza la propiedad "FillColor" para establecer el color del área interior de la forma.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// La propiedad "Opacity" determina cuán transparente es el color en una escala de 0 a 1,
// siendo 1 totalmente opaco y 0 invisible.
// El relleno de la forma por defecto es totalmente opaco, por lo que no podemos ver el texto que está debajo de esta forma.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Establezca la opacidad del color de relleno de la forma a un valor más bajo para que podamos ver el texto debajo de ella.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
