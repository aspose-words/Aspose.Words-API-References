---
title: SaveOptions.DmlEffectsRenderingMode
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML.
type: docs
weight: 60
url: /es/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

### Observaciones

El valor predeterminado esSimplified .

Esta propiedad se utiliza cuando el documento se exporta a formatos de página fijos.

### Ejemplos

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


