---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.SectionLayoutMode per ottimizzare i layout delle sezioni e migliorare il comportamento della griglia del documento per un controllo migliore della formattazione.
type: docs
weight: 6580
url: /it/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Specifica la modalità di layout per una sezione che consente di definire il comportamento della griglia del documento.

```csharp
public enum SectionLayoutMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica che nessuna griglia del documento verrà applicata al contenuto della sezione corrispondente nel documento. |
| Grid | `1` | Specifica che alla sezione corrispondente dovranno essere aggiunti sia il passo di riga che il passo di carattere a ogni riga e carattere al suo interno per mantenere un numero specifico di righe per pagina e di caratteri per riga. I caratteri non verranno allineati automaticamente con le linee della griglia durante la digitazione. |
| LineGrid | `2` | Specifica che alla sezione corrispondente verrà aggiunto un ulteriore passo di riga per ogni riga al suo interno per mantenere il numero specificato di righe per pagina. |
| SnapToChars | `3` | Specifica che alla sezione corrispondente dovranno essere aggiunti sia il passo di riga che il passo di carattere a ogni riga e carattere al suo interno, in modo da mantenere un numero specifico di righe per pagina e di caratteri per riga. I caratteri verranno allineati automaticamente con le linee della griglia durante la digitazione. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
