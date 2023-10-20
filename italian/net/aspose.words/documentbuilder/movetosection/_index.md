---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words per .NET
description: DocumentBuilder MoveToSection metodo. Sposta il cursore allinizio del corpo in una sezione specificata in C#.
type: docs
weight: 570
url: /it/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Sposta il cursore all'inizio del corpo in una sezione specificata.

```csharp
public void MoveToSection(int sectionIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sectionIndex | Int32 | L'indice della sezione in cui spostarsi. |

## Osservazioni

Quando*sectionIndex* è maggiore o uguale a 0, specifica un indice da all'inizio del documento dove 0 è la prima sezione. Quando*sectionIndex* è inferiore a 0, ha specificato un indice dalla fine del documento dove -1 è l'ultima sezione.

Il cursore viene spostato sul primo paragrafo del[`Body`](../../body/) della sezione specificata.

## Esempi

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica che vogliamo intestazioni e piè di pagina diversi per le prime pagine, pari e dispari.
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

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
