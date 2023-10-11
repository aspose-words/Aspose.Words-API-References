---
title: PdfSaveOptions.UseBookFoldPrintingSettings
second_title: Referencia de API de Aspose.Words para .NET
description: PdfSaveOptions propiedad. Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión de folleto si se especifica medianteMultiplePages .
type: docs
weight: 300
url: /es/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Obtiene o establece un valor booleano que indica si el documento debe guardarse usando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Observaciones

Si se especifica esta opción,[`PageSet`](../../fixedpagesaveoptions/pageset/) se ignora al guardar. Este comportamiento coincide con MS Word. Si la configuración de impresión de plegado de libro no se especifica en la configuración de página, esta opción no tendrá ningún efecto.

### Ejemplos

Muestra cómo guardar un documento en formato PDF en forma de libro plegado.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "UseBookFoldPrintingSettings" en "true" para organizar el contenido
// en el PDF de salida de una manera que nos ayude a usarlo para hacer un folleto.
// Establece la propiedad "UseBookFoldPrintingSettings" en "false" para representar el PDF normalmente.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Si renderizamos el documento como un folleto, debemos configurar "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones en "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Una vez que imprimimos este documento en ambos lados de las páginas, podemos doblar todas las páginas por la mitad a la vez,
// y los contenidos se alinearán de forma que se cree un folleto.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfsaveoptions/)
* asamblea [Aspose.Words](../../../)


