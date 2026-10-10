---
title: "Aspose::Words::Shading::get_BackgroundTintAndShade método"
linktitle: "get_BackgroundTintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Shading::get_BackgroundTintAndShade método. Obtiene o establece un valor double que aclara u oscurece un color de tema de fondo en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/shading/get_backgroundtintandshade/
---
## Shading::get_BackgroundTintAndShade method


Obtiene o establece un valor double que aclara u oscurece un color temático de fondo.

```cpp
double Aspose::Words::Shading::get_BackgroundTintAndShade()
```

## Observaciones


Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos



Muestra cómo establecer colores de primer plano y de fondo para la textura de sombreado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## Ver también

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
