---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración Aspose.Words.PdfCustomPropertiesExport mejora las exportaciones de PDF al personalizar las propiedades del documento para obtener resultados óptimos.
type: docs
weight: 6210
url: /es/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Especifica la forma[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) se exportan a archivo PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No se exportan propiedades personalizadas. |
| Standard | `1` | Las propiedades personalizadas se exportan como entradas en el diccionario /Info. |
| Metadata | `2` | Las propiedades personalizadas son metadatos. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
