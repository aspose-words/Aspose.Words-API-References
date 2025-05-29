---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words para .NET
description: Controle la estructura de exportación de su documento con PdfSaveOptions. Administre fácilmente la configuración para optimizar la salida de PDF y optimizar su flujo de trabajo.
type: docs
weight: 140
url: /es/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Obtiene o establece un valor que determina si se debe exportar o no la estructura del documento.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Observaciones

Este valor se ignora al guardar en PDF/A-1a, PDF/A-2a y PDF/UA-1 porque se requiere la estructura del documento para esta conformidad.

Tenga en cuenta que exportar la estructura del documento aumenta significativamente el consumo de memoria, especialmente para los documentos grandes.

## Ejemplos

Muestra cómo preservar los elementos de la estructura del documento, lo que puede ayudar a interpretar programáticamente nuestro documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Establezca la propiedad "ExportDocumentStructure" en "verdadero" para que la estructura del documento, como las etiquetas, estén disponibles a través de
// Panel de navegación "Contenido" de Adobe Acrobat a costa de un mayor tamaño de archivo.
// Establezca la propiedad "ExportDocumentStructure" en "falso" para no exportar la estructura del documento.
options.ExportDocumentStructure = exportDocumentStructure;

// Supongamos que exportamos la estructura del documento al guardarlo. En ese caso,
//podemos abrirlo usando Adobe Acrobat y buscar etiquetas para elementos como el encabezado
// y el siguiente párrafo a través de "Ver" -> "Mostrar/Ocultar" -> "Paneles de navegación" -> "Etiquetas".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
