---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words DmlEffectsRenderingMode para optimizar la representación de efectos DrawingML en formatos de página fijos. ¡Mejore la calidad de sus documentos!
type: docs
weight: 5660
url: /es/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Especifica cómo se representan los efectos de DrawingML en formatos de página fijos.

```csharp
public enum DmlEffectsRenderingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Simplified | `0` | Se simplifica la representación de los efectos de DrawingML. |
| None | `1` | No se renderizan efectos DrawingML. |
| Fine | `2` | Los efectos de DrawingML se procesan en modo fino, lo que implica un procesamiento avanzado. En este modo, la renderización de efectos brinda mejores resultados, pero a un mayor costo de rendimiento queSimplified modo. |

## Ejemplos

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
