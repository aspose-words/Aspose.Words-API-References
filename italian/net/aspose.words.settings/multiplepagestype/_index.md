---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Settings.MultiplePagesType per opzioni di stampa efficienti. Ottimizza il tuo flusso di lavoro con impostazioni di stampa flessibili!
type: docs
weight: 6700
url: /it/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Specifica come viene stampato il documento.

```csharp
public enum MultiplePagesType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | `0` | Stampa normale, nessuna pagina multipla specificata. |
| MirrorMargins | `1` | Scambia i margini sinistro e destro nelle pagine affiancate. |
| TwoPagesPerSheet | `2` | Stampa due pagine per foglio. |
| BookFoldPrinting | `3` | Specifica se stampare il documento come piega a libro. |
| BookFoldPrintingReverse | `4` | Specifica se stampare il documento come piega a libro invertita. |
| Default | `0` | Il valore predefinito èNormal |

## Esempi

Mostra come configurare un documento che può essere stampato come piega a libro.

```csharp
Document doc = new Document();

// Inserisci testo che si estenda su 16 pagine.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configurare la proprietà "PageSetup" della prima sezione per stampare il documento sotto forma di piega a libro.
// Quando stampiamo questo documento su entrambi i lati, possiamo prendere le pagine per impilarle
// e piegali tutti a metà contemporaneamente. Il contenuto del documento si allineerà formando una piega a libro.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Possiamo specificare il numero di fogli solo in multipli di 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
