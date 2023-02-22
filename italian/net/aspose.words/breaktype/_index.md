---
title: Enum BreakType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.BreakType enum. Specifica il tipo di interruzione allinterno di un documento.
type: docs
weight: 100
url: /it/net/aspose.words/breaktype/
---
## BreakType enumeration

Specifica il tipo di interruzione all'interno di un documento.

```csharp
public enum BreakType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ParagraphBreak | `0` | Interruzione tra i paragrafi. |
| PageBreak | `1` | Interruzione di pagina esplicita. |
| ColumnBreak | `2` | Interruzione di colonna esplicita. |
| SectionBreakContinuous | `3` | Specifica l'inizio della nuova sezione nella stessa pagina della sezione precedente. |
| SectionBreakNewColumn | `4` | Specifica l'inizio della nuova sezione nella nuova colonna. |
| SectionBreakNewPage | `5` | Specifica l'inizio di una nuova sezione su una nuova pagina. |
| SectionBreakEvenPage | `6` | Specifica l'inizio di una nuova sezione su una nuova pagina pari. |
| SectionBreakOddPage | `7` | Specifica l'inizio di una nuova sezione su una pagina dispari. |
| LineBreak | `8` | Interruzione di riga esplicita. |

### Esempi

Mostra come creare intestazioni e piè di pagina in un documento utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica che vogliamo intestazioni e piè di pagina diversi per le prime, pari e dispari.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Crea le intestazioni, quindi aggiungi tre pagine al documento per visualizzare ogni tipo di intestazione.
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

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica le proprietà di impostazione della pagina per la sezione corrente del builder e aggiungi del testo.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Se iniziamo una nuova sezione utilizzando un generatore di documenti,
// erediterà le attuali proprietà di configurazione della pagina del builder.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Possiamo ripristinare le sue proprietà di impostazione della pagina ai valori predefiniti utilizzando il metodo "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

Mostra come inserire un sommario (TOC) in un documento utilizzando gli stili di intestazione come voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un sommario per la prima pagina del documento.
// Configura la tabella per raccogliere paragrafi con intestazioni di livello da 1 a 3.
// Inoltre, imposta le sue voci in modo che siano collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il pulsante sinistro del mouse in Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Popolare il sommario aggiungendo paragrafi con stili di intestazione.
// Ciascuna di queste intestazioni con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Un sommario è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


