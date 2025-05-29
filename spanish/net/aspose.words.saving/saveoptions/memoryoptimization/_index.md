---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words para .NET
description: Mejore el rendimiento del documento con la propiedad SaveOptions MemoryOptimization. Controle el uso de memoria antes de guardar, lo que aumenta la eficiencia y la velocidad.
type: docs
weight: 100
url: /es/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Obtiene o establece un valor que determina si se debe realizar la optimización de la memoria antes de guardar el documento. El valor predeterminado para esta propiedad es`FALSO` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Observaciones

Establecer esta opción en`verdadero` Puede reducir significativamente el consumo de memoria al guardar documentos grandes a costa de un tiempo de guardado más lento.

## Ejemplos

Muestra una opción para optimizar el consumo de memoria al convertir documentos grandes a PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Establezca la propiedad "MemoryOptimization" en "verdadero" para reducir el consumo de memoria de las operaciones de guardado de documentos grandes
// a costa de aumentar la duración de la operación.
// Establezca la propiedad "MemoryOptimization" en "falso" para guardar el documento como PDF normalmente.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
