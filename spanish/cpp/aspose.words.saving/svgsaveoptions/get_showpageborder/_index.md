---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder method"
linktitle: "get_ShowPageBorder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder method. Controla si se agrega un borde al contorno de la página. El valor predeterminado es true en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


Controla si se agrega un borde al contorno de la página. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
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
