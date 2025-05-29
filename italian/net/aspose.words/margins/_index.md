---
title: Margins Enum
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Margins per personalizzare i margini dei documenti. Migliora la formattazione dei tuoi documenti con preset facili da usare!
type: docs
weight: 4580
url: /it/net/aspose.words/margins/
---
## Margins enumeration

Specifica i margini preimpostati.

```csharp
public enum Margins
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | `0` | Margini normali. |
| Narrow | `1` | Margini ristretti. |
| Moderate | `2` | Margini moderati. |
| Wide | `3` | Ampi margini. |
| Mirrored | `4` | Margini speculari. |
| Custom | `5` | Margini personalizzati. |

## Esempi

Indica quando ricalcolare il layout di pagina del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Il salvataggio di un documento in PDF, in un'immagine o la stampa per la prima volta verranno eseguiti automaticamente
// memorizza nella cache il layout del documento all'interno delle sue pagine.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificare il documento in qualche modo.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Nella versione corrente di Aspose.Words, la modifica del documento non ne comporta la ricostruzione automatica
// il layout della pagina memorizzato nella cache. Se desideriamo il layout memorizzato nella cache
// Per rimanere aggiornati, dovremo aggiornarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
