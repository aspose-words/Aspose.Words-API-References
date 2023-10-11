---
title: PageSetup.LinesPerPage
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Ottiene o imposta il numero di righe per pagina nella griglia del documento.
type: docs
weight: 240
url: /it/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Ottiene o imposta il numero di righe per pagina nella griglia del documento.

```csharp
public int LinesPerPage { get; set; }
```

### Osservazioni

Il valore minimo della proprietà è 1. Il valore massimo dipende dall'altezza della pagina e dalla dimensione del carattere dello stile Normal . Il passo minimo della riga è pari al 136% della dimensione del carattere. Ad esempio, il numero massimo di righe per pagina di una pagina di lettere con margini di un pollice è 39.

Per impostazione predefinita, la proprietà ha un valore in cui il passo della linea è 1,5 volte maggiore della dimensione del carattere di lo stile Normale.

### Esempi

Mostra come specificare un limite per il numero di righe che ogni pagina può avere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Abilita il pitching, quindi utilizzalo per impostare il numero di righe per pagina in questa sezione.
// Una dimensione del carattere sufficientemente grande spingerà alcune righe verso il basso nella pagina successiva per evitare la sovrapposizione dei caratteri.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


