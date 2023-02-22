---
title: PdfSaveOptions.CustomPropertiesExport
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece un valor que determina el caminoCustomDocumentProperties se exportan a archivo PDF.
type: docs
weight: 50
url: /es/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Obtiene o establece un valor que determina el camino[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) se exportan a archivo PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

### Observaciones

El valor predeterminado esNone.

Metadata el valor no es compatible cuando se guarda en PDF/A. Standard se usará en su lugar para PDF/A-1 y PDF/A-2 y None para PDF/A-4.

Standard el valor no se admite al guardar en PDF 2.0. Metadata se utilizará en su lugar.

### Ejemplos

Muestra cómo exportar propiedades personalizadas al convertir un documento a PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establecer la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.None" para descartar
 // propiedades personalizadas del documento mientras guardamos el documento en .PDF.
// Establecer la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.Standard"
// para conservar las propiedades personalizadas dentro del documento PDF de salida.
// Establecer la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.Metadata"
// para conservar las propiedades personalizadas en un paquete XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Ver también

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


