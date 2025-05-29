---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words per .NET
description: Scopri la proprietà RowFormat AllowBreakAcrossPages, che consente un flusso di testo fluido nelle righe della tabella attraverso le interruzioni di pagina, per una migliore leggibilità e presentazione.
type: docs
weight: 10
url: /it/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Vero se è consentito che il testo in una riga di una tabella venga suddiviso in un'interruzione di pagina.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Esempi

Mostra come disattivare la suddivisione delle righe tra le pagine per ogni riga di una tabella.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Imposta la proprietà "AllowBreakAcrossPages" su "false" per mantenere la riga
// in un unico pezzo se una tabella si estende su due pagine, che si dividono lungo quella riga.
// Se la riga è troppo grande per essere inserita in una pagina, Microsoft Word la sposterà nella pagina successiva.
// Impostare la proprietà "AllowBreakAcrossPages" su "true" per consentire la suddivisione della riga su due pagine.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Guarda anche

* class [RowFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
