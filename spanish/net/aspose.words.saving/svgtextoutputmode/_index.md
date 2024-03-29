---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.SvgTextOutputMode enumeración. Permite especificar cómo se debe representar el texto dentro de un documento al guardarlo en formato SVG en C#.
type: docs
weight: 5610
url: /es/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Permite especificar cómo se debe representar el texto dentro de un documento al guardarlo en formato SVG.

```csharp
public enum SvgTextOutputMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| UseSvgFonts | `0` | Las fuentes SVG se utilizan para representar texto. Tenga en cuenta que no todos los navegadores admiten fuentes SVG. |
| UseTargetMachineFonts | `1` | Las fuentes instaladas en la máquina de destino se utilizan para representar el texto. Nota: si algunas de las fuentes utilizadas en el documento no están disponibles en la máquina de destino, el documento puede verse diferente. |
| UsePlacedGlyphs | `2` | El texto se representa mediante curvas. Tenga en cuenta que la selección de texto no funcionará si utiliza esta opción. |

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
