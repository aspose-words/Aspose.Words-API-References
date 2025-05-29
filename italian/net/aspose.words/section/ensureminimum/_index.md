---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi contenuti con il metodo EnsureMinimum, garantendo che ogni sezione includa un corpo con un paragrafo per maggiore chiarezza e struttura.
type: docs
weight: 150
url: /it/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Assicura che la sezione abbia[`Body`](../body/) con uno[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Esempi

Mostra come preparare un nuovo nodo di sezione per la modifica.

```csharp
Document doc = new Document();

// Un documento vuoto è composto da una sezione, che a sua volta ha un corpo, che a sua volta ha un paragrafo.
// Possiamo aggiungere contenuti a questo documento inserendo elementi come sequenze di testo, forme o tabelle nel paragrafo.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Se aggiungiamo una nuova sezione come questa, non avrà un corpo né altri nodi figlio.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Esegui il metodo "EnsureMinimum" per aggiungere un corpo e un paragrafo a questa sezione per iniziare a modificarla.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
