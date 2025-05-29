---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà LayoutMode di PageSetup per personalizzare facilmente il layout del tuo documento. Migliora il tuo design con opzioni di sezione flessibili!
type: docs
weight: 190
url: /it/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Ottiene o imposta la modalità di layout di questa sezione.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

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

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
