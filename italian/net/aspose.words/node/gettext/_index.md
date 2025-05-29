---
title: Node.GetText
linktitle: GetText
articleTitle: GetText
second_title: Aspose.Words per .NET
description: Scopri il metodo Node GetText per recuperare senza sforzo il testo da un nodo e dai suoi elementi figlio, migliorando la gestione dei dati e l'efficienza dello sviluppo.
type: docs
weight: 120
url: /it/net/aspose.words/node/gettext/
---
## Node.GetText method

Ottiene il testo di questo nodo e di tutti i suoi figli.

```csharp
public virtual string GetText()
```

## Osservazioni

La stringa restituita include tutti i caratteri di controllo e speciali come descritto in[`ControlChar`](../../controlchar/).

## Esempi

Mostra come utilizzare i caratteri di controllo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire paragrafi con testo con DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversione del documento in formato testo rivela che i caratteri di controllo
// rappresentano alcuni elementi strutturali del documento, come le interruzioni di pagina.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Quando si converte un documento in formato stringa,
// possiamo omettere alcuni caratteri di controllo con il metodo Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
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

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
