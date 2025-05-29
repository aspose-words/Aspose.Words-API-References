---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words para .NET
description: Descubra la propiedad UseBookFoldPrintingSettings de PsSaveOptions para guardar fácilmente documentos en un diseño de folleto para una mejor eficiencia de impresión.
type: docs
weight: 30
url: /es/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Obtiene o establece un valor booleano que indica si el documento debe guardarse utilizando un diseño de impresión de folleto, si se especifica mediante[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Observaciones

Si se especifica esta opción,[`PageSet`](../../fixedpagesaveoptions/pageset/) Se ignora al guardar. Este comportamiento coincide con MS Word. Si no se especifican las configuraciones de impresión de plegado de libro en la configuración de página, esta opción no tendrá efecto.

## Ejemplos

Muestra cómo guardar un documento en formato Postscript en forma de libro plegable.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un objeto "PsSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a PostScript.
// Establezca la propiedad "UseBookFoldPrintingSettings" en "true" para organizar el contenido
// en el documento Postscript de salida de manera que nos ayude a hacer un folleto a partir de él.
// Establezca la propiedad "UseBookFoldPrintingSettings" en "false" para guardar el documento normalmente.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Si estamos renderizando el documento como un folleto, debemos configurar "MultiplePages"
// propiedades de los objetos de configuración de página de todas las secciones a "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Una vez que imprimimos este documento en ambos lados de las páginas, podemos doblar todas las páginas por la mitad a la vez,
// y el contenido se alineará de manera que creará un folleto.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Ver también

* class [PsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
