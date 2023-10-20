---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words para .NET
description: PdfSaveOptions CreateNoteHyperlinks propiedad. Especifica si se deben convertir las referencias de notas al pie/notas al final en la historia del texto principal en hipervínculos activos. Cuando se hace clic en el hipervínculo se dirigirá a la nota al pie/nota al final correspondiente. El valor predeterminado esFALSO  en C#.
type: docs
weight: 50
url: /es/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Especifica si se deben convertir las referencias de notas al pie/notas al final en la historia del texto principal en hipervínculos activos. Cuando se hace clic en el hipervínculo, se dirigirá a la nota al pie/nota al final correspondiente. El valor predeterminado es`FALSO` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Ejemplos

Muestra cómo hacer que las notas al pie y al final funcionen como hipervínculos.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "CreateNoteHyperlinks" en "true" para convertir todos los símbolos de notas al pie/notas al final
// en el texto actúan como enlaces que al hacer clic nos llevan a sus respectivas notas al pie/notas al final.
// Establezca la propiedad "CreateNoteHyperlinks" en "false" para que los símbolos de notas al pie/notas al final no se vinculen a nada.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
