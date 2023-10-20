---
title: Section
linktitle: Section
articleTitle: Section
second_title: Aspose.Words per .NET
description: Section costruttore. Inizializza una nuova istanza della classe Sezione in C#.
type: docs
weight: 10
url: /it/net/aspose.words/section/section/
---
## Section constructor

Inizializza una nuova istanza della classe Sezione.

```csharp
public Section(DocumentBase doc)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |

## Osservazioni

Quando la sezione viene creata, appartiene al documento specificato, ma non è ancora parte del documento e[`ParentNode`](../../node/parentnode/) È`nullo`.

Includere[`Section`](../) in un utilizzo del documento[`InsertAfter`](../../compositenode/insertafter/) e [`InsertBefore`](../../compositenode/insertbefore/) metodi del[`Document`](../../document/) OR [`Add`](../../nodecollection/add/) E[`Insert`](../../nodecollection/insert/) metodi del[`Sections`](../../document/sections/) proprietà.

## Esempi

Mostra come costruire manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti questi nodi,
// e finiamo con un nodo documento senza figli.
doc.RemoveAllChildren();

// Questo documento ora non ha nodi secondari compositi a cui possiamo aggiungere contenuto.
// Se desideriamo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Innanzitutto, crea una nuova sezione, quindi aggiungila come figlia al nodo del documento root.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione necessita di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi lo aggiunge come figlio al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per realizzare il documento. Crea una corsa,
// ne imposta l'aspetto e il contenuto, quindi lo aggiunge come figlio al paragrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Guarda anche

* class [DocumentBase](../../documentbase/)
* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
