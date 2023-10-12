---
title: Enum TableStyleOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Tables.TableStyleOptions enum. Specifica la modalità di applicazione dello stile tabella a una tabella.
type: docs
weight: 6370
url: /it/net/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enumeration

Specifica la modalità di applicazione dello stile tabella a una tabella.

```csharp
[Flags]
public enum TableStyleOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Non viene applicata alcuna formattazione dello stile tabella. |
| FirstRow | `20` | Applica la formattazione condizionale della prima riga. |
| LastRow | `40` | Applica la formattazione condizionale dell'ultima riga. |
| FirstColumn | `80` | Applica 1 formattazione condizionale alla prima colonna. |
| LastColumn | `100` | Applica la formattazione condizionale dell'ultima colonna. |
| RowBands | `200` | Applica la formattazione condizionale per la suddivisione delle righe. |
| ColumnBands | `400` | Applica la formattazione condizionale per la suddivisione delle colonne. |
| Default2003 | `600` | Viene applicata la suddivisione di righe e colonne. Questa è l'impostazione predefinita di Microsoft Word per i vecchi formati come DOC, WML e RTF. |
| Default | `2A0` | Queste sono le impostazioni predefinite di Microsoft Word. |

### Esempi

Mostra come creare una nuova tabella durante l'applicazione di uno stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Dobbiamo inserire almeno una riga prima di impostare qualsiasi formattazione della tabella.
builder.InsertCell();

// Imposta lo stile della tabella utilizzato in base all'identificatore dello stile.
// Tieni presente che non tutti gli stili di tabella sono disponibili quando si salva nel formato .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Applica parzialmente lo stile alle funzionalità della tabella in base ai predicati, quindi crea la tabella.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

### Guarda anche

* property [StyleOptions](../table/styleoptions/)
* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)


