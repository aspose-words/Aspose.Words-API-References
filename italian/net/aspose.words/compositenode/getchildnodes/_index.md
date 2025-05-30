---
title: CompositeNode.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words per .NET
description: Scopri il metodo CompositeNode GetChildNodes recupera senza sforzo una raccolta live di nodi figlio personalizzati in base al tipo specificato per prestazioni migliorate.
type: docs
weight: 110
url: /it/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | NodeType | Specifica il tipo di nodi da selezionare. |
| isDeep | Boolean | `VERO` per selezionare ricorsivamente da tutti i nodi figlio; `falso` per selezionare solo tra i figli più prossimi. |

### Valore di ritorno

Una raccolta live di nodi figlio del tipo specificato.

## Osservazioni

La raccolta di nodi restituita da questo metodo è sempre attiva.

Una raccolta live è sempre sincronizzata con il documento. Ad esempio, se selezioni tutte le sezioni di un documento e le enumeri nella raccolta eliminandole, la sezione verrà rimossa immediatamente dalla raccolta quando verrà rimossa dal documento.

## Esempi

Mostra come stampare tutti i commenti di un documento e le relative risposte.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Se un commento non ha antenati, si tratta di un commento di "livello superiore" e non di un commento di tipo risposta.
// Stampa tutti i commenti di primo livello insieme alle eventuali risposte.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file singoli.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Ottieni la raccolta di forme dal documento,
// e salva i dati dell'immagine di ogni forma con un'immagine come file nel file system locale.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // I dati immagine delle forme possono contenere immagini di molti possibili formati.
        // Possiamo determinare automaticamente un'estensione di file per ogni immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
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

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
