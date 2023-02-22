---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
second_title: Referencia de API de Aspose.Words para .NET
description: MetafileRenderingOptions propiedad. Obtiene o establece un valor que determina cómo se deben representar los metarchivos EMF Dual.
type: docs
weight: 20
url: /es/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Obtiene o establece un valor que determina cómo se deben representar los metarchivos EMF+ Dual.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

### Observaciones

Los metarchivos duales EMF+ contienen partes EMF+ y EMF. MS Word y GDI+ siempre representan la parte EMF+. Aspose.Words actualmente no es totalmente compatible con todos los registros EMF+ y, en algunos casos, el resultado de la representación de la parte EMF se ve mejor que el resultado de la representación de la parte EMF+.

Esta opción se usa solo cuando el metarchivo se representa como gráficos vectoriales. Cuando el metarchivo se representa en mapa de bits, siempre se utiliza la parte EMF+.

El valor predeterminado esEmfPlusWithFallback.

### Ejemplos

Muestra cómo configurar las opciones de representación relacionadas con el metarchivo mejorado de Windows al guardar en PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establecer la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.Emf"
// para renderizar solo la parte EMF de un metarchivo dual EMF+.
// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlus" para
// para representar la parte EMF+ de un metarchivo dual EMF+.
// Establecer la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// para representar la parte EMF+ de un metarchivo dual EMF+ si se admiten todos los registros EMF+.
// De lo contrario, Aspose.Words representará la parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Establezca la propiedad "UseEmfEmbeddedToWmf" en "true" para representar datos EMF incrustados
// para metarchivos que podemos representar como gráficos vectoriales.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ver también

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../metafilerenderingoptions/)
* asamblea [Aspose.Words](../../../)


