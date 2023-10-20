---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words para .NET
description: MetafileRenderingOptions EmfPlusDualRenderingMode propiedad. Obtiene o establece un valor que determina cómo se deben representar los metarchivos duales EMF en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Obtiene o establece un valor que determina cómo se deben representar los metarchivos duales EMF+.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Observaciones

Los metarchivos duales EMF+ contienen partes EMF+ y EMF. MS Word y GDI+ siempre representan la parte EMF+. Aspose.Words actualmente no es totalmente compatible con todos los registros EMF+ y, en algunos casos, la representación del resultado de la parte EMF se ve mejor que la representación del resultado de la parte EMF+.

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales. Cuando el metarchivo se renderiza en mapa de bits, siempre se utiliza la parte EMF+.

El valor predeterminado esEmfPlusWithFallback.

## Ejemplos

Muestra cómo configurar las opciones de representación mejoradas relacionadas con el metarchivo de Windows al guardar en PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establece la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.Emf"
// para representar solo la parte EMF de un metarchivo dual EMF+.
// Establece la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlus" para
// para representar la parte EMF+ de un metarchivo dual EMF+.
// Establece la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// para representar la parte EMF+ de un metarchivo dual EMF+ si todos los registros EMF+ son compatibles.
// De lo contrario, Aspose.Words representará la parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Establece la propiedad "UseEmfEmbeddedToWmf" en "true" para representar datos EMF incrustados
// para metarchivos que podemos representar como gráficos vectoriales.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ver también

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
