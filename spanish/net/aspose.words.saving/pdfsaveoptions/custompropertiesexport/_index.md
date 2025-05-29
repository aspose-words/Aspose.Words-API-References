---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PdfSaveOptions CustomPropertiesExport mejora sus exportaciones de PDF al controlar CustomDocumentProperties para obtener resultados óptimos.
type: docs
weight: 70
url: /es/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Obtiene o establece un valor que determina la forma[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) se exportan a archivo PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Observaciones

El valor predeterminado esNone.

Metadata El valor no es compatible al guardar en PDF/A. Standard Se utilizará en su lugar para PDF/A-1 y PDF/A-2 y None para PDF/A-4.

Standard El valor no es compatible al guardar en PDF 2.0. Metadata Se utilizará en su lugar.

## Ejemplos

Muestra cómo exportar propiedades personalizadas al convertir un documento a PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.None" para descartarla
// Propiedades del documento personalizadas cuando guardamos el documento en .PDF.
// Establezca la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.Standard"
// para conservar propiedades personalizadas dentro del documento PDF de salida.
// Establezca la propiedad "CustomPropertiesExport" en "PdfCustomPropertiesExport.Metadata"
// para conservar propiedades personalizadas en un paquete XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Ver también

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
