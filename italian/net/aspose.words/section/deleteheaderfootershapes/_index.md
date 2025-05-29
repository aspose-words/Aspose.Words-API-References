---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo tutte le forme di disegno dalle intestazioni e dai piè di pagina delle sezioni con il metodo DeleteHeaderFooterShapes, per una presentazione più pulita del documento.
type: docs
weight: 140
url: /it/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Elimina tutte le forme (oggetti di disegno) dalle intestazioni e dai piè di pagina di questa sezione.

```csharp
public void DeleteHeaderFooterShapes()
```

## Esempi

Mostra come rimuovere tutte le forme da tutte le intestazioni e i piè di pagina di una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un'intestazione primaria con una forma.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Crea un piè di pagina principale con un'immagine.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// Rimuovere tutte le forme dalle intestazioni e dai piè di pagina nella prima sezione.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
