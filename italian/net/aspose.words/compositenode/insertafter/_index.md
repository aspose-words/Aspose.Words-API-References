---
title: CompositeNode.InsertAfter
linktitle: InsertAfter
articleTitle: InsertAfter
second_title: Aspose.Words per .NET
description: Inserisci nodi senza sforzo con il metodo InsertAfter di CompositeNode, migliorando la gestione della struttura dati e garantendo un posizionamento efficiente dei nodi.
type: docs
weight: 150
url: /it/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter&lt;T&gt; method

Inserisce il nodo specificato subito dopo il nodo di riferimento specificato.

```csharp
public T InsertAfter<T>(T newChild, Node refChild)
    where T : Node
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| newChild | T | IL[`Node`](../../node/) da inserire. |
| refChild | Node | IL[`Node`](../../node/) che è il nodo di riferimento. Il*newChild* è posto dopo il*refChild*. |

### Valore di ritorno

Il nodo inserito.

## Osservazioni

Se*refChild* È`null` , inserti*newChild* all'inizio dell'elenco dei nodi figlio.

Se il*newChild* è già presente nell'albero, prima viene rimosso.

Se il nodo inserito è stato creato da un altro documento, dovresti usare [`ImportNode`](../../documentbase/importnode/) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

## Esempi

Mostra come sostituire tutte le forme delle caselle di testo con forme di immagini.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

Mostra come aggiungere, aggiornare ed eliminare nodi figlio nella raccolta di nodi figlio di un CompositeNode.

```csharp
Document doc = new Document();

// Per impostazione predefinita, un documento vuoto contiene un paragrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// I nodi compositi come il nostro paragrafo possono contenere altri nodi compositi e inline come figli.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea altri tre nodi di esecuzione.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Il corpo del documento non visualizzerà queste esecuzioni finché non le inseriremo in un nodo composito
// che a sua volta fa parte dell'albero dei nodi del documento, come abbiamo fatto con la prima esecuzione.
// Possiamo determinare dove si trova il contenuto di testo dei nodi che inseriamo
// appare nel documento specificando una posizione di inserimento relativa a un altro nodo nel paragrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserire la seconda esecuzione nel paragrafo che precede quella iniziale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserisce la terza esecuzione dopo quella iniziale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserisce la prima esecuzione all'inizio della raccolta di nodi figlio del paragrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Possiamo modificare il contenuto dell'esecuzione modificando ed eliminando i nodi figlio esistenti.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
