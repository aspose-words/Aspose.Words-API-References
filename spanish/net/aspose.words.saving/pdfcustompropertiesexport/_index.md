---
title: Enum PdfCustomPropertiesExport
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfCustomPropertiesExport enumeración. Especifica la formaCustomDocumentProperties se exportan a archivo PDF.
type: docs
weight: 5140
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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


