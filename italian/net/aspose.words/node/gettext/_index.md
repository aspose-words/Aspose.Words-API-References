---
title: Node.GetText
second_title: Aspose.Words per .NET API Reference
description: Node metodo. Ottiene il testo di questo nodo e di tutti i suoi figli.
type: docs
weight: 120
url: /it/net/aspose.words/node/gettext/
---
## Node.GetText method

Ottiene il testo di questo nodo e di tutti i suoi figli.

```csharp
public virtual string GetText()
```

### Osservazioni

La stringa restituita include tutti i caratteri di controllo e speciali come descritto in[`ControlChar`](../../controlchar/).

### Esempi

Mostra come usare i caratteri di controllo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci paragrafi con testo con DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversione del documento in formato testo rivela che i caratteri di controllo
// rappresentano alcuni degli elementi strutturali del documento, come le interruzioni di pagina.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Quando si converte un documento in formato stringa,
// possiamo omettere alcuni dei caratteri di controllo con il metodo Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
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

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../node/)
* assemblea [Aspose.Words](../../../)


