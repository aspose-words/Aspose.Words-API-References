---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.MarkdownExportAsHtml per convertire senza sforzo gli elementi Markdown in HTML grezzo, migliorando le opzioni di esportazione dei documenti.
type: docs
weight: 6020
url: /it/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Consente di specificare gli elementi da esportare in Markdown come HTML grezzo.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Esporta tutti gli elementi utilizzando la sintassi Markdown senza alcun codice HTML grezzo. |
| Tables | `1` | Esporta le tabelle come HTML grezzo. |

## Esempi

Mostra come esportare una tabella in Markdown come HTML grezzo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Crea tabella.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
