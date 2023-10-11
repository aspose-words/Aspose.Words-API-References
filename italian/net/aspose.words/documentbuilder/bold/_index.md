---
title: DocumentBuilder.Bold
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder proprietà. Vero se il carattere è formattato in grassetto.
type: docs
weight: 20
url: /it/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Vero se il carattere è formattato in grassetto.

```csharp
public bool Bold { get; set; }
```

### Esempi

Mostra come riempire MERGEFIELD con dati con un generatore di documenti invece che con una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce alcuni MERGEFIELDS, che accettano dati da colonne con lo stesso nome in un'origine dati durante una stampa unione,
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
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


