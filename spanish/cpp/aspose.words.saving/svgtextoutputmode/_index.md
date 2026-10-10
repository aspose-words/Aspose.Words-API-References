---
title: "Enumeración Aspose::Words::Saving::SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Saving::SvgTextOutputMode. Permite especificar cómo se debe renderizar el texto dentro de un documento al guardarlo en formato SVG en C++."
type: docs
weight: 83000
url: /es/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


Permite especificar cómo debe renderizarse el texto dentro de un documento al guardarlo en formato SVG.

```cpp
enum class SvgTextOutputMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseSvgFonts | 0 | Se utilizan fuentes SVG para renderizar texto. Nota, no todos los navegadores admiten fuentes SVG. |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) instaladas en la máquina objetivo se utilizan para renderizar texto. Nota, si algunas de las fuentes usadas en el documento no están disponibles en la máquina objetivo, el documento puede mostrarse de forma diferente. |
| UsePlacedGlyphs | 2 | El texto se renderiza usando curvas. Nota, la selección de texto no funcionará si usa esta opción. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
