---
title: Enum SectionLayoutMode
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.SectionLayoutMode enum. Specifica la modalità di layout per una sezione consentendo di definire il comportamento della griglia del documento.
type: docs
weight: 5750
url: /it/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Specifica la modalità di layout per una sezione consentendo di definire il comportamento della griglia del documento.

```csharp
public enum SectionLayoutMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica che non verrà applicata alcuna griglia del documento al contenuto della sezione corrispondente del documento. |
| Grid | `1` | Specifica che la sezione corrispondente avrà sia il passo di riga aggiuntivo che il passo di carattere aggiunti a ciascuna riga e carattere al suo interno per mantenere un numero specifico di righe per pagina e caratteri per riga. I caratteri non verranno allineati automaticamente con le linee della griglia su digitando. |
| LineGrid | `2` | Specifica che la sezione corrispondente avrà un passo di riga aggiuntivo aggiunto a ciascuna riga al suo interno per mantenere il numero specificato di righe per pagina. |
| SnapToChars | `3` | Specifica che la sezione corrispondente dovrà avere sia il passo di riga aggiuntivo che il passo di carattere aggiunti a ciascuna riga e carattere al suo interno per mantenere un numero specifico di righe per pagina e caratteri per riga. I caratteri verranno allineati automaticamente alla griglia durante la digitazione. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


