---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words para .NET
description: Descubra cómo Aspose.Words.Saving.DmlRenderingMode mejora la representación de formas de DrawingML para formatos de página fijos de alta calidad. ¡Optimice el aspecto visual de sus documentos!
type: docs
weight: 5670
url: /es/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Especifica cómo se representan las formas de DrawingML en formatos de página fijos.

```csharp
public enum DmlRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Fallback | `0` | Si la forma de respaldo está disponible para DrawingML, Aspose.Words representa la forma de respaldo en lugar de DrawingML. |
| DrawingML | `1` | Aspose.Words ignora la forma de respaldo de DrawingML y renderiza el propio DrawingML. Este es el modo predeterminado. |

## Ejemplos

Muestra cómo renderizar formas de respaldo al guardar en PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "DmlRenderingMode" en "DmlRenderingMode.Fallback"
// para sustituir las formas DML con sus formas de reserva.
// Establezca la propiedad "DmlRenderingMode" en "DmlRenderingMode.DrawingML"
// para representar las formas DML en sí.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Muestra cómo configurar la calidad de representación de los efectos DrawingML en un documento cuando lo guardamos en PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "DmlEffectsRenderingMode" en "DmlEffectsRenderingMode.None" para descartar todos los efectos DrawingML.
// Establezca la propiedad "DmlEffectsRenderingMode" en "DmlEffectsRenderingMode.Simplified"
// para representar una versión simplificada de los efectos de DrawingML.
// Establezca la propiedad "DmlEffectsRenderingMode" en "DmlEffectsRenderingMode.Fine" para
// renderiza efectos DrawingML con mayor precisión y también con mayor costo de procesamiento.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
