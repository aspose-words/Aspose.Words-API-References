---
title: PdfSaveOptions.Compliance
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Especifica el nivel de cumplimiento de los estándares PDF para los documentos de salida.
type: docs
weight: 40
url: /es/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Especifica el nivel de cumplimiento de los estándares PDF para los documentos de salida.

```csharp
public PdfCompliance Compliance { get; set; }
```

### Observaciones

El valor predeterminado esPdf17.

### Ejemplos

Muestra cómo configurar el nivel de cumplimiento de los estándares PDF de los documentos PDF guardados.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
// Tenga en cuenta que algunas PdfSaveOptions están prohibidas al guardar en uno de los estándares y se corrigen automáticamente.
// Utilice IWarningCallback para saber qué opciones se corrigen automáticamente.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Establece la propiedad "Cumplimiento" en "PdfCompliance.PdfA1b" para cumplir con el estándar "PDF/A-1b",
// cuyo objetivo es preservar la apariencia visual del documento mientras Aspose.Words lo convierte a PDF.
// Establezca la propiedad "Cumplimiento" en "PdfCompliance.Pdf17" para cumplir con el estándar "1.7".
// Establece la propiedad "Cumplimiento" en "PdfCompliance.PdfA1a" para cumplir con el estándar "PDF/A-1a",
// que cumple con "PDF/A-1b" además de preservar la estructura del documento original.
// Establezca la propiedad "Cumplimiento" en "PdfCompliance.PdfUa1" para cumplir con el estándar "PDF/UA-1" (ISO 14289-1).
// que tiene como objetivo definir representar documentos electrónicos en PDF que permitan que el archivo sea accesible.
// Establezca la propiedad "Cumplimiento" en "PdfCompliance.Pdf20" para cumplir con el estándar "PDF 2.0" (ISO 32000-2).
// Establezca la propiedad "Cumplimiento" en "PdfCompliance.PdfA4" para cumplir con el estándar "PDF/A-4" (ISO 19004:2020).
// que preserva la apariencia visual estática del documento a lo largo del tiempo.
// Esto ayuda a que los documentos se puedan buscar, pero puede aumentar significativamente el tamaño de documentos que ya son grandes.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Ver también

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


