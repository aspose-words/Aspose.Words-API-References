---
title: PageSetup.SectionStart
linktitle: SectionStart
articleTitle: SectionStart
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageSetup SectionStart per gestire facilmente le interruzioni di sezione nel tuo documento. Migliora la formattazione e il controllo del layout oggi stesso!
type: docs
weight: 390
url: /it/net/aspose.words/pagesetup/sectionstart/
---
## PageSetup.SectionStart property

Restituisce o imposta il tipo di interruzione di sezione per l'oggetto specificato.

```csharp
public SectionStart SectionStart { get; set; }
```

## Esempi

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

Mostra come specificare in che modo una nuova sezione si separa dalla precedente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// I tipi di interruzione di sezione determinano il modo in cui una nuova sezione si separa da quella precedente.
// Di seguito sono riportati cinque tipi di interruzioni di sezione.
// 1 - Inizia la sezione successiva su una nuova pagina:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Avvia la sezione successiva nella pagina corrente:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Inizia la sezione successiva su una nuova pagina pari:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Inizia la sezione successiva su una nuova pagina dispari:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Avvia la sezione successiva su una nuova colonna:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Guarda anche

* enum [SectionStart](../../sectionstart/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
