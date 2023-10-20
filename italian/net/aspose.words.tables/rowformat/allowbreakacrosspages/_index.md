---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words per .NET
description: RowFormat AllowBreakAcrossPages proprietà. Vero se il testo in una riga di tabella può essere suddiviso in uninterruzione di pagina in C#.
type: docs
weight: 10
url: /it/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Vero se il testo in una riga di tabella può essere suddiviso in un'interruzione di pagina.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Esempi

Mostra come disabilitare la suddivisione delle righe tra le pagine per ogni riga di una tabella.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Imposta la proprietà "AllowBreakAcrossPages" su "false" per mantenere la riga
// tutto intero se una tabella si estende su due pagine, che si suddividono lungo quella riga.
// Se la riga è troppo grande per stare in una pagina, Microsoft Word la spingerà alla pagina successiva.
// Imposta la proprietà "AllowBreakAcrossPages" su "true" per consentire la suddivisione della riga su due pagine.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Guarda anche

* class [RowFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
