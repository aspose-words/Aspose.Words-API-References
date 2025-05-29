---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SaveOptions DmlEffectsRenderingMode optimiza la representación de efectos DrawingML para mejorar el rendimiento y la calidad del documento.
type: docs
weight: 60
url: /es/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

Obtiene o establece un valor que determina cómo se representan los efectos de DrawingML.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Observaciones

El valor predeterminado esSimplified .

Esta propiedad se utiliza cuando el documento se exporta a formatos de página fijos.

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
