---
title: Document.EnsureMinimum
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Se il documento non contiene sezioni crea una sezione con un paragrafo.
type: docs
weight: 600
url: /it/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Se il documento non contiene sezioni, crea una sezione con un paragrafo.

```csharp
public void EnsureMinimum()
```

### Esempi

Mostra come garantire che un documento contenga il set minimo di nodi richiesti per modificarne il contenuto.

```csharp
// Un documento appena creato contiene una sezione figlia, che include un corpo figlio e un paragrafo figlio.
// Possiamo modificare il contenuto del corpo del documento aggiungendo nodi come Sequenze o Forme in linea a quel paragrafo.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Questo è l'insieme minimo di nodi di cui abbiamo bisogno per poter modificare il documento.
// Non saremo più in grado di modificare il documento se ne rimuoviamo qualcuno.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Chiama questo metodo per assicurarti che il documento abbia almeno questi tre nodi in modo da poterlo modificare nuovamente.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


