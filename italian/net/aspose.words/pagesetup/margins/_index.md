---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words per .NET
description: PageSetup Margins proprietà. Restituisce o imposta il presetMargins della pagina in C#.
type: docs
weight: 260
url: /it/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

Restituisce o imposta il preset[`Margins`](../../margins/) della pagina.

```csharp
public Margins Margins { get; set; }
```

## Esempi

Mostra quando ricalcolare il layout di pagina del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Il salvataggio di un documento in PDF, in un'immagine o la stampa per la prima volta avverrà automaticamente
// memorizza nella cache il layout del documento all'interno delle sue pagine.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifica il documento in qualche modo.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // Nella versione corrente di Aspose.Words, la modifica del documento non viene ricostruita automaticamente
// il layout della pagina memorizzata nella cache. Se desideriamo il layout memorizzato nella cache
// per rimanere aggiornati, dovremo aggiornarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Guarda anche

* enum [Margins](../../margins/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
