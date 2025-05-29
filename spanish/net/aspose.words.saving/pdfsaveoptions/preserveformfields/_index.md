---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PreserveFormFields de PdfSaveOptions conserva los campos de formulario de Microsoft Word en archivos PDF o los convierte a texto. ¡Mejore la calidad de sus documentos!
type: docs
weight: 280
url: /es/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Especifica si se deben conservar los campos de formulario de Microsoft Word como campos de formulario en PDF o convertirlos en texto. El valor predeterminado es`FALSO` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Observaciones

Los campos de formulario de Microsoft Word incluyen controles de entrada de texto, menús desplegables y casillas de verificación.

Cuando se establece en`FALSO` Estos campos se exportarán como texto a PDF. Cuando se configuran como`verdadero`, estos campos se exportarán como campos de formulario PDF.

Al exportar campos de formulario a PDF como campos de formulario, puede producirse cierta pérdida de formato porque los campos PDF form no admiten todas las funciones de los campos de formulario de Microsoft Word.

Además, el tamaño de salida depende del tamaño del contenido porque los formularios editables en Microsoft Word son objetos en línea.

Los formularios editables están prohibidos por la conformidad con PDF/A.`FALSO` El valor se utilizará automáticamente al guardar en PDF/A.

Los campos de formulario no son compatibles al guardar en PDF/UA.`FALSO` El valor se utilizará automáticamente.

## Ejemplos

Muestra cómo guardar un documento en formato PDF utilizando el método Save y la clase PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Inserte un cuadro combinado que permitirá al usuario elegir una opción de una colección de cadenas.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Establezca la propiedad "PreserveFormFields" en "true" para guardar los campos de formulario como objetos interactivos en el PDF de salida.
// Establezca la propiedad "PreserveFormFields" en "false" para congelar todos los campos de formulario en el documento en
// sus valores actuales y mostrarlos como texto simple en el PDF de salida.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
