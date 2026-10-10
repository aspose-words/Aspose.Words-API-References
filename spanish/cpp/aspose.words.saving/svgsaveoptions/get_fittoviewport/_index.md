---
title: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort method"
linktitle: "get_FitToViewPort"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort method. Especifica si el SVG de salida debe llenar el área disponible del viewport (ventana del navegador o contenedor). Cuando se establece en true, el ancho y alto del SVG de salida se configuran al 100%. El valor predeterminado es false en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


Especifica si el SVG de salida debe llenar el área de vista disponible (ventana del navegador o contenedor). Cuando se establece en **true**, el ancho y la altura del SVG de salida se fijan al 100 %. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


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

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
