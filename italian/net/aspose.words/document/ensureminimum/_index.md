---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo EnsureMinimum per creare automaticamente una sezione e un paragrafo nei documenti, assicurando contenuti completi e organizzati.
type: docs
weight: 620
url: /it/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Se il documento non contiene sezioni, crea una sezione con un paragrafo.

```csharp
public void EnsureMinimum()
```

## Esempi

Mostra come garantire che un documento contenga il set minimo di nodi richiesti per modificarne il contenuto.

```csharp
// Un documento appena creato contiene una Sezione figlia, che include un Corpo figlia e un Paragrafo figlia.
// Possiamo modificare il contenuto del corpo del documento aggiungendo nodi come Runs o forme in linea a quel paragrafo.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Questo è il set minimo di nodi di cui abbiamo bisogno per poter modificare il documento.
// Se rimuoviamo uno di questi elementi, non saremo più in grado di modificare il documento.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Chiama questo metodo per assicurarti che il documento abbia almeno quei tre nodi, così da poterlo modificare di nuovo.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
