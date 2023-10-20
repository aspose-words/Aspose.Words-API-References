---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words per .NET
description: Body EnsureMinimum metodo. Se lultimo figlio non è un paragrafo crea e aggiunge un paragrafo vuoto in C#.
type: docs
weight: 50
url: /it/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto.

```csharp
public void EnsureMinimum()
```

## Esempi

Cancella il testo principale da tutte le sezioni del documento lasciando le sezioni stesse.

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

// Una sezione necessita di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Questo corpo non ha figli, quindi non possiamo ancora aggiungergli esecuzioni.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Chiama "EnsureMinimum" per assicurarsi che questo corpo contenga almeno un paragrafo vuoto.
body.EnsureMinimum();

// Ora possiamo aggiungere sequenze al corpo e fare in modo che il documento le visualizzi.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [Body](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
