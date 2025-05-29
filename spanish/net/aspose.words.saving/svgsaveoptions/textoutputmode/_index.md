---
title: SvgSaveOptions.TextOutputMode
linktitle: TextOutputMode
articleTitle: TextOutputMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad TextOutputMode de SvgSaveOptions, que controla la representación de texto en SVG para una mejor calidad visual y personalización. ¡Optimice sus gráficos hoy mismo!
type: docs
weight: 120
url: /es/net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Obtiene o establece un valor que determina cómo se debe representar el texto en SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Observaciones

Utilice esta propiedad para obtener o establecer el modo en que debe representarse el texto dentro de un documento al guardar en formato SVG.

El valor predeterminado esUseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
