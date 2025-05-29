---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.HeaderFooterType per identificare facilmente i tipi di intestazione e piè di pagina nei documenti Word. Migliora l'elaborazione dei tuoi documenti oggi stesso!
type: docs
weight: 3550
url: /it/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Identifica il tipo di intestazione o piè di pagina trovato in un file Word.

```csharp
public enum HeaderFooterType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| HeaderEven | `0` | Intestazione per le pagine pari. |
| HeaderPrimary | `1` | Intestazione primaria, utilizzata anche per le pagine dispari. |
| FooterEven | `2` | Piè di pagina per le pagine pari. |
| FooterPrimary | `3` | Piè di pagina principale, utilizzato anche per le pagine dispari. |
| HeaderFirst | `4` | Intestazione per la prima pagina della sezione. |
| FooterFirst | `5` | Piè di pagina per la prima pagina della sezione. |

## Esempi

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare che si vogliono intestazioni e piè di pagina diversi per la prima pagina, le pagine pari e quelle dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ciascun tipo di intestazione.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
