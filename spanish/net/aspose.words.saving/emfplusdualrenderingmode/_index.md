---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración EMF Plus Dual Rendering Mode de Aspose.Words para una óptima representación de metarchivos EMF Dual. ¡Mejore el procesamiento de sus documentos con precisión!
type: docs
weight: 5730
url: /es/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Especifica cómo Aspose.Words debe representar los metarchivos duales EMF+.

```csharp
public enum EmfPlusDualRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words intenta representar la parte EMF+ del metarchivo EMF+ Dual. Si algunos registros EMF+ no son compatibles, Aspose.Words representa la parte EMF del metarchivo EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words representa EMF+ como parte del metarchivo EMF+ Dual. |
| Emf | `2` | Aspose.Words representa la parte EMF del metarchivo dual EMF+. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
