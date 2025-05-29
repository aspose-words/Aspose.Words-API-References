---
title: PageSetup.PaperSize
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageSetup PaperSize per personalizzare e gestire facilmente il formato carta del tuo documento per ottenere risultati di stampa ottimali.
type: docs
weight: 350
url: /it/net/aspose.words/pagesetup/papersize/
---
## PageSetup.PaperSize property

Restituisce o imposta il formato della carta.

```csharp
public PaperSize PaperSize { get; set; }
```

## Osservazioni

L'impostazione di questa proprietà aggiorna[`PageWidth`](../pagewidth/) E[`PageHeight`](../pageheight/) valori. Impostando questo valore suCustom non modifica i valori esistenti.

## Esempi

Mostra come impostare il formato carta JisB4 o JisB5.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

PageSetup pageSetup = doc.FirstSection.PageSetup;
// Imposta il formato della carta su JisB4 (257x364mm).
pageSetup.PaperSize = PaperSize.JisB4;
// In alternativa, impostare il formato carta su JisB5. (182x257mm).
pageSetup.PaperSize = PaperSize.JisB5;
```

Mostra come regolare il formato della carta, l'orientamento, i margini e altre impostazioni per una sezione.

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

// Possiamo modificare la dimensione della pagina corrente in una dimensione predefinita
// utilizzando la proprietà "PaperSize" dell'oggetto PageSetup di questa sezione.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// Ogni sezione ha il suo oggetto PageSetup. Quando utilizziamo un generatore di documenti per creare una nuova sezione,
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

Mostra come creare manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e si finisce con un nodo documento senza elementi figlio.
doc.RemoveAllChildren();

// Questo documento non ha più nodi figlio compositi a cui aggiungere contenuto.
// Se volessimo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlia al nodo radice del documento.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e poi aggiungilo come elemento secondario al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per completare il documento. Crea una run,
// impostane l'aspetto e il contenuto, quindi aggiungilo come elemento figlio al paragrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Guarda anche

* enum [PaperSize](../../papersize/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
