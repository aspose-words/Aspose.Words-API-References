---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words para .NET
description: Mejore sus archivos PDF con CreateNoteHyperlinks de PdfSaveOptions. Convierta notas al pie y notas finales en enlaces interactivos para facilitar la navegación. Valor predeterminado falso.
type: docs
weight: 60
url: /es/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Especifica si se deben convertir las referencias de notas al pie o notas al final del texto principal en hipervínculos activos. Al hacer clic, el hipervínculo llevará a la nota al pie o nota al final correspondiente. El valor predeterminado es`FALSO` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Ejemplos

Muestra cómo hacer que las notas al pie y las notas finales funcionen como hipervínculos.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "CreateNoteHyperlinks" en "verdadero" para convertir todos los símbolos de notas al pie/notas finales
// en el texto actúan como enlaces que, al hacer clic, nos llevan a sus respectivas notas a pie de página/notas finales.
// Establezca la propiedad "CreateNoteHyperlinks" en "falso" para que los símbolos de notas al pie o notas finales no se vinculen a nada.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
