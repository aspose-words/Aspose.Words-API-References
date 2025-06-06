---
title: SvgSaveOptions.FitToViewPort
linktitle: FitToViewPort
articleTitle: FitToViewPort
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FitToViewPort de SvgSaveOptions optimiza su salida SVG para llenar perfectamente cualquier ventana o contenedor del navegador y obtener imágenes impactantes.
type: docs
weight: 30
url: /es/net/aspose.words.saving/svgsaveoptions/fittoviewport/
---
## SvgSaveOptions.FitToViewPort property

Especifica si el SVG de salida debe llenar el área de la ventana gráfica disponible (ventana del navegador o contenedor). Cuando se establece en`verdadero`El ancho y la altura del SVG de salida se establecen al 100%.

El valor predeterminado es`FALSO`.

```csharp
public bool FitToViewPort { get; set; }
```

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

* class [SvgSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
