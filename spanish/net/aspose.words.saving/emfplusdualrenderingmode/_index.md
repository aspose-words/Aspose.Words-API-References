---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.EmfPlusDualRenderingMode enumeración. Especifica cómo Aspose.Words debe representar los metarchivos duales EMF en C#.
type: docs
weight: 4980
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
| EmfPlusWithFallback | `0` | Aspose.Words intenta representar EMF+ como parte del metarchivo dual EMF+. Si algunos de los registros EMF+ no son compatibles , entonces Aspose.Words representa EMF como parte del metarchivo dual EMF+. |
| EmfPlus | `1` | Aspose.Words representa EMF+ como parte del metarchivo dual EMF+. |
| Emf | `2` | Aspose.Words representa EMF como parte del metarchivo dual EMF+. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
