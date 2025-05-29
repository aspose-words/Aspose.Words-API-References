---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PdfSaveOptions DisplayDocTitle mejora su experiencia con PDF al mostrar los títulos de los documentos en la barra de título de Windows para una fácil identificación.
type: docs
weight: 90
url: /es/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Un indicador que especifica si la barra de título de la ventana debe mostrar el título del documento tomado de la entrada Título del diccionario de información del documento.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Observaciones

Si`FALSO`, la barra de título debería mostrar el nombre del archivo PDF que contiene el documento.

Esta bandera es requerida por el cumplimiento de PDF/UA.`verdadero` El valor se utilizará automáticamente al guardar en PDF/UA.

El valor predeterminado es`FALSO`.

## Ejemplos

Muestra cómo mostrar el título del documento como la barra de título.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
// Establezca "DisplayDocTitle" en "verdadero" para obtener algunos lectores de PDF, como Adobe Acrobat Pro,
// para mostrar el valor de la propiedad incorporada "Título" del documento en la pestaña que pertenece a este documento.
// Establezca "DisplayDocTitle" en "falso" para que dichos lectores muestren el nombre de archivo del documento.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
