---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad EmfPlusDualRenderingMode mejora la representación de metarchivos EMF Dual. ¡Optimice sus gráficos con opciones de representación flexibles hoy mismo!
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

Los metarchivos duales EMF+ contienen tanto EMF+ como partes EMF. MS Word y GDI+ siempre procesan la parte EMF+. Aspose.Words actualmente no es totalmente compatible con todos los registros EMF+ y, en algunos casos, el resultado de la representación de la parte EMF se ve mejor que el de la parte EMF+.

Esta opción solo se utiliza cuando el metarchivo se renderiza como gráfico vectorial. Cuando el metarchivo se renderiza como mapa de bits, siempre se utiliza la parte EMF+.

El valor predeterminado esEmfPlusWithFallback.

## Ejemplos

Muestra cómo configurar las opciones de representación relacionadas con el metarchivo mejorado de Windows al guardar en PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.Emf"
// para representar únicamente la parte EMF de un metarchivo dual EMF+.
// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlus" para
// para representar la parte EMF+ de un metarchivo dual EMF+.
// Establezca la propiedad "EmfPlusDualRenderingMode" en "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// para representar la parte EMF+ de un metarchivo dual EMF+ si se admiten todos los registros EMF+.
// De lo contrario, Aspose.Words representará la parte EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Establezca la propiedad "UseEmfEmbeddedToWmf" en "verdadero" para representar datos EMF incrustados
// para metarchivos que podemos representar como gráficos vectoriales.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ver también

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
