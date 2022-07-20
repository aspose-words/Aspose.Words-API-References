---
title: Node
second_title: Aspose.Words per .NET API Reference
description: Classe base per tutti i nodi di un documento Word.
type: docs
weight: 3930
url: /it/net/aspose.words/node/
---
## Node class

Classe base per tutti i nodi di un documento Word.

```csharp
public abstract class Node
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ottiene il documento a cui appartiene questo nodo. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Restituisce vero se questo nodo può contenere altri nodi. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Ottiene il tipo di questo nodo. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ottiene il nodo immediatamente precedente a questo nodo. |
| [Range](../../aspose.words/node/range) { get; } | Restituisce a **Gamma** oggetto che rappresenta la parte di un documento contenuta in questo nodo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone)(bool) | Crea un duplicato del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor#getancestor)(NodeType) | Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor#getancestor_1)(Type) | Ottiene il primo predecessore del tipo di oggetto specificato. |
| virtual [GetText](../../aspose.words/node/gettext)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero di preordine. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ottiene il nodo precedente in base all'algoritmo di attraversamento dell'albero di preordine. |
| [Remove](../../aspose.words/node/remove)() | Si rimuove dal genitore. |
| [ToString](../../aspose.words/node/tostring#tostring_1)(SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring#tostring_2)(SaveOptions) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring)(NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa facile da usare. |

### Osservazioni

Un documento è rappresentato come un albero di nodi, simile a DOM o XmlDocument.

Per ulteriori informazioni, vedere il modello di progettazione Composite.

Il[`Node`](../node)classe:

* Definisce l'interfaccia del nodo figlio.
* Definisce l'interfaccia per visitare i nodi.
* Fornisce la capacità di clonazione predefinita.
* Implementa i meccanismi del nodo padre e del documento proprietario.
* Implementa l'accesso ai nodi di pari livello.

### Esempi

Mostra come rimuovere tutti i nodi figlio di un tipo specifico da un nodo composito.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Salva il prossimo nodo di pari livello come variabile nel caso in cui desideriamo spostarci su di esso dopo aver eliminato questo nodo.
    Node nextNode = curNode.NextSibling;

    // Un corpo di sezione può contenere nodi Paragrafo e Tabella.
    // Se il nodo è una tabella, rimuoverlo dal genitore.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

Mostra come clonare un nodo composito.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Di seguito sono riportati due modi per clonare un nodo composito.
// 1 - Crea un clone di un nodo e crea anche un clone di ciascuno dei suoi nodi figlio.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Crea un clone di un nodo da solo senza figli.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

Mostra come attraversare la raccolta di nodi figlio di un nodo composito.

```csharp
Document doc = new Document();

// Aggiungi due esecuzioni e una forma come nodi figlio al primo paragrafo di questo documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo durante la vita del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Scorri la raccolta del paragrafo dei figli immediati,
// e stampa qualsiasi traccia o forma che troviamo all'interno.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
