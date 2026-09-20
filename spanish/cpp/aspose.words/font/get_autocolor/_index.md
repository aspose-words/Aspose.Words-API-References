---
title: "Método Aspose::Words::Font::get_AutoColor"
linktitle: "get_AutoColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_AutoColor. Devuelve el color calculado actual del texto (negro o blanco) que se usará para ''auto color''. Si el color no es ''auto'' entonces devuelve Color en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Devuelve el color calculado actual del texto (negro o blanco) que se usará para 'auto color'. Si el color no es 'auto' entonces devuelve [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Observaciones


Cuando el texto tiene 'color automático', el color real del texto se calcula automáticamente para que sea legible contra el color de fondo. Al cambiar el color de fondo, el color del texto cambiará automáticamente a negro o blanco en MS Word para maximizar la legibilidad.

## Ejemplos



Muestra cómo mejorar la legibilidad seleccionando automáticamente el color del texto según el brillo de su fondo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si el objeto Font de una ejecución no especifica el color del texto, lo hará automáticamente
// seleccionará negro o blanco dependiendo del color del fondo.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// El color predeterminado del texto es negro. Si el color del fondo es oscuro, el texto negro será difícil de ver.
// Para resolver este problema, la propiedad AutoColor mostrará este texto en blanco.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Si cambiamos el fondo a un color claro, el negro será un
// color de texto más adecuado que el blanco, de modo que el auto color lo mostrará en negro.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
