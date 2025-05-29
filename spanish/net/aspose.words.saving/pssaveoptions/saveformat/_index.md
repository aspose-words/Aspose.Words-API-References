---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveFormat de PsSaveOptions para especificar fácilmente el formato de guardado de su documento. ¡Optimice su flujo de trabajo con opciones de guardado flexibles!
type: docs
weight: 20
url: /es/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedePs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
