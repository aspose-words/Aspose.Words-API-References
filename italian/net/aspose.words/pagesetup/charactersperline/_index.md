---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words per .NET
description: Controlla il layout del tuo documento con la proprietà CharactersPerLine di PageSetup. Regola facilmente i caratteri per riga per una leggibilità e un design ottimali.
type: docs
weight: 100
url: /it/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Ottiene o imposta il numero di caratteri per riga nella griglia del documento.

```csharp
public int CharactersPerLine { get; set; }
```

## Osservazioni

Il valore minimo della proprietà è 1. Il valore massimo dipende dalla larghezza della pagina e dalla dimensione del carattere dello stile Normal . Il passo minimo del carattere è il 90% della dimensione del carattere. Ad esempio, il numero massimo di caratteri per riga di una pagina Letter con margini di un pollice è 43.

Per impostazione predefinita, la proprietà ha un valore in cui il passo del carattere è uguale alla dimensione del font dello stile Normal .

## Esempi

Mostra come specificare il numero di caratteri che ogni riga può contenere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Abilita il pitching e poi usalo per impostare il numero di caratteri per riga in questa sezione.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Il numero di caratteri dipende anche dalla dimensione del font.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
