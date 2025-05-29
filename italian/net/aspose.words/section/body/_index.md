---
title: Section.Body
linktitle: Body
articleTitle: Body
second_title: Aspose.Words per .NET
description: Scopri la proprietà Corpo della sezione che recupera il nodo figlio Corpo, migliorando lo sviluppo web con una gestione semplificata dei contenuti.
type: docs
weight: 20
url: /it/net/aspose.words/section/body/
---
## Section.Body property

Restituisce il[`Body`](../../body/) nodo figlio della sezione.

```csharp
public Body Body { get; }
```

## Osservazioni

[`Body`](../../body/) contiene il testo principale della sezione.

Resi`null` se la sezione non ha un[`Body`](../../body/) nodo tra i suoi figli.

## Esempi

Cancella il testo principale da tutte le sezioni del documento, lasciando inalterate le sezioni stesse.

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

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Questo corpo non ha elementi figlio, quindi non possiamo ancora aggiungergli esecuzioni.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Chiama "EnsureMinimum" per assicurarti che questo corpo contenga almeno un paragrafo vuoto.
body.EnsureMinimum();

// Ora possiamo aggiungere le esecuzioni al corpo e fare in modo che il documento le visualizzi.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [Body](../../body/)
* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
