---
title: CompositeNode.GetChild
second_title: Aspose.Words per .NET API Reference
description: CompositeNode metodo. Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato.
type: docs
weight: 100
url: /it/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Restituisce un Nesimo nodo figlio che corrisponde al tipo specificato.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | NodeType | Specifica il tipo del nodo figlio. |
| index | Int32 | Indice in base zero del nodo figlio da selezionare. Sono consentiti anche indici negativi e indicano l'accesso dalla fine, ovvero -1 indica l'ultimo nodo. |
| isDeep | Boolean | `VERO` per selezionare ricorsivamente da tutti i nodi figlio; `falso`selezionare solo tra i figli immediati. Vedi i commenti per maggiori informazioni. |

### Valore di ritorno

Il nodo figlio che corrisponde ai criteri o`nullo` se non viene trovato alcun nodo corrispondente.

### Osservazioni

Se l'indice è fuori intervallo, a`nullo` viene restituito.

Tieni presente che i nodi di markup (StructuredDocumentTag ESmartTag ) vengono attraversati anche quando*isDeep* =`falso` E`GetChild` viene richiamato per il tipo di nodo non markup. Ad esempio, se la prima esecuzione in un para è racchiusa in a[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , verrà comunque restituito entro`GetChild`(Run , 0,`falso`).

### Esempi

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

// Questo metodo riguarda le proprietà dello stile della tabella come quelle impostate sopra.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Mostra come attraversare la raccolta di nodi figlio di un nodo composito.

```csharp
Document doc = new Document();

// Aggiungi due sequenze e una forma come nodi secondari al primo paragrafo di questo documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Tieni presente che "CustomNodeId" non viene salvato in un file di output ed esiste solo durante la durata del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Scorrere la raccolta dei figli immediati del paragrafo,
// e stampa tutte le sequenze o le forme che troviamo all'interno.
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
* spazio dei nomi [Aspose.Words](../../compositenode/)
* assemblea [Aspose.Words](../../../)


