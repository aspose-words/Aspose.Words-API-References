---
title: Enum PaperSize
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.PaperSize enum. Specifica il formato carta.
type: docs
weight: 4140
url: /it/net/aspose.words/papersize/
---
## PaperSize enumeration

Specifica il formato carta.

```csharp
public enum PaperSize
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| A3 | `0` | 297 x 420 mm. |
| A4 | `1` | 210 x 297 mm. |
| A5 | `2` | 148 x 210 mm. |
| B4 | `3` | 250 x 353 mm. |
| B5 | `4` | 176 x 250 mm. |
| Executive | `5` | 7,25 x 10,5 pollici. |
| Folio | `6` | 8,5 x 13 pollici. |
| Ledger | `7` | 17 x 11 pollici. |
| Legal | `8` | 8,5 x 14 pollici. |
| Letter | `9` | 8,5 x 11 pollici. |
| EnvelopeDL | `10` | 110 x 220 mm. |
| Quarto | `11` | 8,47 x 10,83 pollici. |
| Statement | `12` | 8,5 x 5,5 pollici. |
| Tabloid | `13` | 11 x 17 pollici. |
| Paper10x14 | `14` | 10 x 14 pollici. |
| Paper11x17 | `15` | 11 x 17 pollici. |
| Number10Envelope | `16` | 4,125 x 9,5 pollici. |
| Custom | `17` | Formato carta personalizzato. |

### Esempi

Mostra come regolare il formato carta, l'orientamento, i margini e altre impostazioni per una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Mostra come impostare le dimensioni della pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo cambiare la dimensione della pagina corrente in una dimensione predefinita
// utilizzando la proprietà "PaperSize" dell'oggetto PageSetup di questa sezione.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Ogni sezione ha il proprio oggetto PageSetup. Quando utilizziamo un generatore di documenti per creare una nuova sezione,
// l'oggetto PageSetup di quella sezione eredita tutti i valori dell'oggetto PageSetup della sezione precedente.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// Imposta una dimensione personalizzata per le pagine di questa sezione.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

Mostra come costruire manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e finisci con un nodo documento senza figli.
doc.RemoveAllChildren();

// Questo documento ora non ha nodi figlio compositi a cui possiamo aggiungere contenuto.
// Se desideriamo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Innanzitutto, crea una nuova sezione, quindi aggiungila come figlio al nodo del documento radice.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per fare il documento. Crea una corsa,
// imposta l'aspetto e il contenuto, quindi aggiungilo come figlio al paragrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


