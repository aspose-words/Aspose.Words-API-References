---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words para .NET
description: Descubra la propiedad PdfSaveOptions UseBookFoldPrintingSettings para guardar fácilmente documentos en un diseño de folleto para una mejor eficiencia de impresión.
type: docs
weight: 320
url: /es/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Obtiene o establece un valor booleano que indica si el documento debe guardarse utilizando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Observaciones

Si se especifica esta opción,[`PageSet`](../../fixedpagesaveoptions/pageset/) Se ignora al guardar. Este comportamiento coincide con MS Word. Si no se especifican las configuraciones de impresión de plegado de libro en la configuración de página, esta opción no tendrá efecto.

## Ejemplos

Muestra cómo guardar un documento en formato PDF en forma de libro plegable.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "UseBookFoldPrintingSettings" en "true" para organizar el contenido
// en el PDF de salida de una manera que nos ayude a usarlo para hacer un folleto.
// Establezca la propiedad "UseBookFoldPrintingSettings" en "false" para representar el PDF normalmente.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Si estamos renderizando el documento como un folleto, debemos configurar "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Una vez que imprimimos este documento en ambos lados de las páginas, podemos doblar todas las páginas por la mitad a la vez,
// y el contenido se alineará de manera que creará un folleto.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
