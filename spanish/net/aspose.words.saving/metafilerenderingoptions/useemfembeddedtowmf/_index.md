---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words para .NET
description: MetafileRenderingOptions UseEmfEmbeddedToWmf propiedad. Obtiene o establece un valor que determina cómo se deben representar los metarchivos WMF con metarchivos EMF incrustados en C#.
type: docs
weight: 70
url: /es/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Obtiene o establece un valor que determina cómo se deben representar los metarchivos WMF con metarchivos EMF incrustados.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Observaciones

Los metarchivos WMF podrían contener datos EMF incrustados. MS Word en la mayoría de los casos usa datos EMF incrustados. GDI+ siempre usa datos WMF.

Cuando este valor se establece en`verdadero`, Aspose.Words utiliza datos EMF incrustados al renderizar.

Cuando este valor se establece en`FALSO`, Aspose.Words utiliza datos WMF al renderizar.

Esta opción se utiliza sólo cuando el metarchivo se representa como gráficos vectoriales. Cuando el metarchivo se renderiza en mapa de bits, siempre se utilizan datos WMF.

El valor predeterminado es`verdadero`.

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

* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
