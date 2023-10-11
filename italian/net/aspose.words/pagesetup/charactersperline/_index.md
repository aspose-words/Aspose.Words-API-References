---
title: PageSetup.CharactersPerLine
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Ottiene o imposta il numero di caratteri per riga nella griglia del documento.
type: docs
weight: 100
url: /it/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Ottiene o imposta il numero di caratteri per riga nella griglia del documento.

```csharp
public int CharactersPerLine { get; set; }
```

### Osservazioni

Il valore minimo della proprietà è 1. Il valore massimo dipende dalla larghezza della pagina e dalla dimensione del carattere dello stile Normal . La spaziatura minima del carattere è pari al 90% della dimensione del carattere. Ad esempio, il numero massimo di caratteri per riga di una pagina di lettere con margini di un pollice è 43.

Per impostazione predefinita, la proprietà ha un valore in base al quale la spaziatura del carattere è uguale alla dimensione del carattere dello stile Normal .

### Esempi

Mostra come specificare a per il numero di caratteri che ciascuna riga può contenere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Abilita il pitching, quindi utilizzalo per impostare il numero di caratteri per riga in questa sezione.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Il numero di caratteri dipende anche dalla dimensione del carattere.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


