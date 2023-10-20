---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words para .NET
description: PdfSaveOptions CustomPropertiesExport propiedad. Obtiene o establece un valor que determina la formaCustomDocumentProperties se exportan a un archivo PDF en C#.
type: docs
weight: 60
url: /es/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Obtiene o establece un valor que determina la forma[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) se exportan a un archivo PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Observaciones

El valor predeterminado esNone.

Metadata el valor no se admite al guardar en PDF/A. Standard se utilizará en su lugar para PDF/A-1 y PDF/A-2 y None para PDF/A-4.

Standard el valor no se admite al guardar en PDF 2.0. Metadata se utilizará en su lugar.

## Ejemplos

Muestra cómo exportar propiedades personalizadas al convertir un documento a PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.None" para descartar
// propiedades personalizadas del documento a medida que guardamos el documento en .PDF.
// Establece la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.Standard"
// para preservar las propiedades personalizadas dentro del documento PDF de salida.
// Establece la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.Metadata"
// para preservar las propiedades personalizadas en un paquete XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Ver también

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
