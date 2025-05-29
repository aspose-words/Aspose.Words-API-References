---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.DocumentBuilderOptions per migliorare la creazione dei tuoi documenti con funzionalità personalizzabili per un'esperienza di creazione fluida.
type: docs
weight: 670
url: /it/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Consente di specificare opzioni aggiuntive per il processo di creazione del documento.

```csharp
public class DocumentBuilderOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che la segue. Il valore predefinito è`VERO` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Corrisponde alla modalità di progettazione in Microsoft Word. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
