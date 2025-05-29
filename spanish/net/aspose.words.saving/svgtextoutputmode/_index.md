---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.SvgTextOutputMode para personalizar la representación de texto en formato SVG, mejorando la presentación del documento y el atractivo visual.
type: docs
weight: 6410
url: /es/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Permite especificar cómo debe representarse el texto dentro de un documento al guardar en formato SVG.

```csharp
public enum SvgTextOutputMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseSvgFonts | `0` | Las fuentes SVG se utilizan para representar texto. Tenga en cuenta que no todos los navegadores las admiten. |
| UseTargetMachineFonts | `1` | Las fuentes instaladas en la máquina de destino se utilizan para representar el texto. Tenga en cuenta que, si algunas de las fuentes utilizadas en el documento no están disponibles en la máquina de destino, el documento puede tener un aspecto diferente. |
| UsePlacedGlyphs | `2` | El texto se renderiza mediante curvas. Nota: la selección de texto no funcionará si usa esta opción. |

## Ejemplos

Muestra cómo imitar las propiedades de las imágenes al convertir un documento .docx a .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configure el objeto SvgSaveOptions para guardar sin bordes de página ni texto seleccionable.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
