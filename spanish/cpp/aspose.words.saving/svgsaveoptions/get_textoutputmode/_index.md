---
title: "Método Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode"
linktitle: "get_TextOutputMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode. Obtiene o establece un valor que determina cómo se debe renderizar el texto en SVG en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


Obtiene o establece un valor que determina cómo se debe renderizar el texto en SVG.

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## Observaciones


Utilice esta propiedad para obtener o establecer el modo en que el texto dentro de un documento debe renderizarse al guardarse en formato SVG.

El valor predeterminado es [UseTargetMachineFonts](../../svgtextoutputmode/).

## Ejemplos



Muestra cómo imitar las propiedades de las imágenes al convertir un documento .docx a .svg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Configure el objeto SvgSaveOptions para guardar sin bordes de página ni texto seleccionable.
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## Ver también

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
