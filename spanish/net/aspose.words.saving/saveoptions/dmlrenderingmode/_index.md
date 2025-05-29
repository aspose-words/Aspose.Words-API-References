---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SaveOptions DmlRenderingMode mejora la representación de formas de DrawingML. ¡Optimice el aspecto visual de sus documentos sin esfuerzo!
type: docs
weight: 70
url: /es/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Obtiene o establece un valor que determina cómo se representan las formas de DrawingML.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## Observaciones

El valor predeterminado esFallback .

Esta propiedad se utiliza cuando el documento se exporta a formatos de página fijos.

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
