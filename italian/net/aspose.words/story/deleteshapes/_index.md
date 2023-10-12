---
title: Story.DeleteShapes
second_title: Aspose.Words per .NET API Reference
description: Story metodo. Elimina tutte le forme dal testo di questa storia.
type: docs
weight: 70
url: /it/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Elimina tutte le forme dal testo di questa storia.

```csharp
public void DeleteShapes()
```

### Esempi

Mostra come rimuovere tutte le forme da un nodo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un DocumentBuilder per inserire una forma. Questa è una forma in linea,
// che ha un Paragrafo genitore, che è un nodo figlio del Corpo della prima sezione.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Possiamo eliminare tutte le forme dai paragrafi figlio di questo Body.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* class [Story](../)
* spazio dei nomi [Aspose.Words](../../story/)
* assemblea [Aspose.Words](../../../)


