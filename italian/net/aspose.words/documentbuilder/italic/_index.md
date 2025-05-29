---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words per .NET
description: Scopri la proprietà Corsivo di DocumentBuilder. Formatta facilmente il tuo testo in corsivo per migliorare la leggibilità e lo stile dei tuoi documenti.
type: docs
weight: 140
url: /it/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

Vero se il font è formattato in corsivo.

```csharp
public bool Italic { get; set; }
```

## Esempi

Mostra come riempire i MERGEFIELD con dati tramite un generatore di documenti anziché tramite una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire alcuni MERGEFIELDS, che accettano dati da colonne con lo stesso nome in un'origine dati durante una stampa unione,
// e poi riempirli manualmente.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
