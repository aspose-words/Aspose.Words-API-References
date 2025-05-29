---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words per .NET
description: Scopri la proprietà ContextTableFormatting in DocumentBuilderOptions. Assicurati che la formattazione delle tabelle rimanga indipendente, migliorando la chiarezza e lo stile del tuo documento.
type: docs
weight: 20
url: /it/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che la segue. Il valore predefinito è`VERO` .

```csharp
public bool ContextTableFormatting { get; set; }
```

## Esempi

Mostra come ignorare la formattazione della tabella per il contenuto successivo.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Aggiunge contenuto prima della tabella.
// La dimensione predefinita del carattere è 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Modifica la dimensione del carattere all'interno della tabella.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Se ContextTableFormatting è true, la formattazione della tabella non viene applicata al contenuto successivo.
// Se ContextTableFormatting è falso, la formattazione della tabella viene applicata al contenuto successivo.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Guarda anche

* class [DocumentBuilderOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
