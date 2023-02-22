---
title: PdfSaveOptions.PreserveFormFields
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Especifica si se conservarán los campos de formulario de Microsoft Word como campos de formulario en PDF o si se convertirán en texto. El valor predeterminado esfalso .
type: docs
weight: 240
url: /es/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Especifica si se conservarán los campos de formulario de Microsoft Word como campos de formulario en PDF o si se convertirán en texto. El valor predeterminado es`falso` .

```csharp
public bool PreserveFormFields { get; set; }
```

### Observaciones

Los campos de formulario de Microsoft Word incluyen controles de entrada de texto, menús desplegables y casillas de verificación.

cuando se establece en`falso` , estos campos se exportarán como texto a PDF. cuando se establece en`verdadero`, estos campos se exportarán como campos de formulario PDF.

Al exportar campos de formulario a PDF como campos de formulario, es posible que se produzca alguna pérdida de formato porque los campos form de PDF no son compatibles con todas las funciones de los campos de formulario de Microsoft Word.

Además, el tamaño de salida depende del tamaño del contenido porque los formularios editables en Microsoft Word son objetos en línea .

Los formularios editables están prohibidos por el cumplimiento de PDF/A.`falso` El valor se utilizará automáticamente al guardar en PDF/A.

Los campos de formulario no se admiten al guardar en PDF/UA.`falso` valor se utilizará automáticamente.

### Ejemplos

Muestra cómo guardar un documento en formato PDF mediante el método Guardar y la clase PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Inserte un cuadro combinado que permitirá al usuario elegir una opción de una colección de cadenas.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Establezca la propiedad "PreserveFormFields" en "true" para guardar campos de formulario como objetos interactivos en el PDF de salida.
// Establezca la propiedad "PreserveFormFields" en "false" para congelar todos los campos de formulario en el documento en
// sus valores actuales y mostrarlos como texto sin formato en el PDF de salida.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


