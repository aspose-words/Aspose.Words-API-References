---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words per .NET
description: Controlla il layout del tuo documento con la proprietà LinesPerPage di PageSetup. Regola facilmente le righe per pagina per una leggibilità e un'organizzazione ottimali.
type: docs
weight: 240
url: /it/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Ottiene o imposta il numero di righe per pagina nella griglia del documento.

```csharp
public int LinesPerPage { get; set; }
```

## Osservazioni

Il valore minimo della proprietà è 1. Il valore massimo dipende dall'altezza della pagina e dalla dimensione del carattere dello stile Normal . La spaziatura minima è il 136% della dimensione del carattere. Ad esempio, il numero massimo di righe per pagina di una pagina Letter con margini di un pollice è 39.

Per impostazione predefinita, la proprietà ha un valore in base al quale il passo della riga è 1,5 volte maggiore della dimensione del carattere dello stile Normale .

## Esempi

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Abilita il pitching e poi usalo per impostare il numero di righe per pagina in questa sezione.
// Una dimensione del carattere sufficientemente grande sposterà alcune righe sulla pagina successiva per evitare la sovrapposizione di caratteri.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
