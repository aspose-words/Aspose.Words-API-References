---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words per .NET
description: Scopri il metodo CompositeNode GetChild per recuperare facilmente l'ennesimo nodo figlio di un tipo specifico, migliorando l'efficienza della gestione dei dati.
type: docs
weight: 100
url: /it/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Restituisce un N-esimo nodo figlio che corrisponde al tipo specificato.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | NodeType | Specifica il tipo di nodo figlio. |
| index | Int32 | Indice basato su zero del nodo figlio da selezionare. Sono consentiti anche indici negativi che indicano l'accesso dalla fine, ovvero -1 indica l'ultimo nodo. |
| isDeep | Boolean | `VERO` per selezionare ricorsivamente da tutti i nodi figlio; `falso` Per selezionare solo tra i figli diretti. Vedi le osservazioni per maggiori informazioni. |

### Valore di ritorno

Il nodo figlio che corrisponde ai criteri o`null` se non viene trovato alcun nodo corrispondente.

## Osservazioni

Se l'indice è fuori intervallo, a`null` viene restituito.

Nota che i nodi di markup (StructuredDocumentTag ESmartTag ) vengono attraversati anche quando*isDeep* =`falso` E`GetChild` viene invocato per il tipo di nodo non di markup. Ad esempio, se la prima esecuzione in un para è racchiusa in un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , verrà comunque restituito da`GetChild`(Run , 0,`falso`).

## Esempi

Mostra come applicare le proprietà dello stile di una tabella direttamente agli elementi della tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Questo metodo riguarda le proprietà di stile della tabella come quelle che abbiamo impostato sopra.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Mostra come attraversare la raccolta di nodi figlio di un nodo composito.

```csharp
Document doc = new Document();

// Aggiungere due sequenze e una forma come nodi figlio al primo paragrafo di questo documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo per la durata del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Scorrere la raccolta di elementi figlio immediati del paragrafo,
// e stampare tutte le sequenze o le forme che troviamo al suo interno.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Guarda anche

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
