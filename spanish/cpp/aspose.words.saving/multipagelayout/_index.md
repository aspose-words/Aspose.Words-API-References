---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MultiPageLayout class. Define un diseño para renderizar múltiples páginas en una sola salida en C++."
type: docs
weight: 14500
url: /es/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Define un diseño para renderizar múltiples páginas en una única salida.

```cpp
class MultiPageLayout : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Obtiene el color de fondo de la salida. El valor predeterminado es **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Obtiene el color del borde de las páginas. El valor predeterminado es **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Obtiene el ancho del borde de las páginas. El valor predeterminado es 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Crea un diseño en el que las páginas se renderizan de izquierda a derecha, de arriba a abajo, en una cuadrícula con el número especificado de columnas. |
| static [Horizontal](./horizontal/)(float) | Crea un diseño en el que todas las páginas especificadas se renderizan horizontalmente una al lado de la otra, de izquierda a derecha, en una sola salida. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Establece el color de fondo de la salida. El valor predeterminado es **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Establece el color del borde de las páginas. El valor predeterminado es **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Establece el ancho del borde de las páginas. El valor predeterminado es 0. |
| static [SinglePage](./singlepage/)() | Crea un diseño que renderiza solo la primera de las páginas especificadas. |
| static [TiffFrames](./tiffframes/)() | Crea un diseño donde cada página se renderiza como un marco separado en una imagen TIFF multicuadro. Aplicable solo a formatos de imagen TIFF. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Crea un diseño donde todas las páginas especificadas se renderizan verticalmente una debajo de la otra en una única salida. |

## Ejemplos



Muestra cómo guardar el documento en una imagen JPG con configuraciones de diseño de varias páginas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Configura un diseño de cuadrícula con:
// - 3 columnas por fila.
// - Espaciado de 10 pts entre páginas (horizontal y vertical).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Diseños alternativos:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Personaliza el fondo y el borde.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
