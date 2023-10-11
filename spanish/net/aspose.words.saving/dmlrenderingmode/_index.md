---
title: Enum DmlRenderingMode
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.DmlRenderingMode enumeración. Especifica cómo se representan las formas de DrawingML en formatos de página fijos.
type: docs
weight: 4920
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
| Fallback | `0` | Si la forma alternativa está disponible para DrawingML, Aspose.Words representa la forma alternativa en lugar de DrawingML. |
| DrawingML | `1` | Aspose.Words ignora la forma alternativa de DrawingML y representa el propio DrawingML. Este es el modo predeterminado. |

### Ejemplos

Muestra cómo representar formas alternativas al guardar en PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "DmlRenderingMode" en "DmlRenderingMode.Fallback"
// para sustituir formas DML con sus formas alternativas.
// Establece la propiedad "DmlRenderingMode" en "DmlRenderingMode.DrawingML"
// para representar las formas DML mismas.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Muestra cómo configurar la calidad de representación de los efectos de DrawingML en un documento mientras lo guardamos en PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "DmlEffectsRenderingMode" en "DmlEffectsRenderingMode.None" para descartar todos los efectos de DrawingML.
// Establece la propiedad "DmlEffectsRenderingMode" en "DmlEffectsRenderingMode.Simplified"
// para representar una versión simplificada de los efectos de DrawingML.
// Establece la propiedad "DmlEffectsRenderingMode" en "DmlEffectsRenderingMode.Fine" para
// renderiza los efectos de DrawingML con más precisión y también con más costo de procesamiento.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


