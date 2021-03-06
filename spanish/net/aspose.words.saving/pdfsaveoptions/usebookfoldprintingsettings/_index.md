---
title: UseBookFoldPrintingSettings
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece un valor booleano que indica si el documento debe guardarse utilizando un diseño de impresión de folleto si se especifica medianteMultiplePagesaspose.words/pagesetup/multiplepages .
type: docs
weight: 270
url: /es/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Obtiene o establece un valor booleano que indica si el documento debe guardarse utilizando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Observaciones

Si se especifica esta opción,[`PageSet`](../../fixedpagesaveoptions/pageset) se ignora al guardar. Este comportamiento coincide con MS Word. Si la configuración de impresión de plegado de libro no se especifica en la configuración de página, esta opción no tendrá efecto.

### Ejemplos

Muestra cómo guardar un documento en formato PDF en forma de libro plegado.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establecer la propiedad "UseBookFoldPrintingSettings" en "true" para organizar el contenido
// en el PDF de salida de una manera que nos ayude a usarlo para hacer un folleto.
// Establezca la propiedad "UseBookFoldPrintingSettings" en "falso" para representar el PDF normalmente.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Si estamos renderizando el documento como un folleto, debemos configurar las "Páginas Múltiples"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Una vez que imprimamos este documento en ambos lados de las páginas, podemos doblar todas las páginas por la mitad a la vez,
// y el contenido se alineará de forma que se cree un folleto.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../../pdfsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
