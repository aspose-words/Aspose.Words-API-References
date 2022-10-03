---
title: GetChildNodes
second_title: Aspose.Words per .NET API Reference
description: Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato.
type: docs
weight: 100
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
| isDeep | Boolean | True per selezionare ricorsivamente da tutti i nodi figlio. Falso per selezionare solo tra i figli immediati. |

### Valore di ritorno

Una raccolta live di nodi figlio del tipo specificato.

### Osservazioni

La raccolta di nodi restituiti da questo metodo è sempre attiva.

Una raccolta live è sempre sincronizzata con il documento. Ad esempio, se hai selezionato tutte le sezioni in un documento ed enumerato attraverso la raccolta eliminando le sezioni, la sezione viene rimossa dalla raccolta immediatamente quando viene rimossa dal documento.

### Esempi

Mostra come stampare tutti i commenti di un documento e le relative risposte.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Se un commento non ha predecessori, è un commento di "livello superiore" anziché un commento di tipo risposta.
// Stampa tutti i commenti di primo livello insieme a tutte le risposte che potrebbero avere.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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

Mostra come estrarre immagini da un documento e salvarle nel file system locale come singoli file.

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
        // I dati immagine delle forme possono contenere immagini di molti possibili formati immagine. 
        // Possiamo determinare automaticamente un'estensione di file per ogni immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Mostra come aggiungere, aggiornare ed eliminare nodi figlio in una raccolta di figli di CompositeNode.

```csharp
Document doc = new Document();

// Un documento vuoto, per impostazione predefinita, ha un paragrafo.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// I nodi compositi come il nostro paragrafo possono contenere altri nodi compositi e inline come figli.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Crea altri tre nodi di esecuzione.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Il corpo del documento non visualizzerà queste esecuzioni finché non le inseriamo in un nodo composito
// che di per sé fa parte dell'albero dei nodi del documento, come abbiamo fatto con la prima esecuzione.
// Possiamo determinare dove si trova il contenuto del testo dei nodi che inseriamo
// appare nel documento specificando una posizione di inserimento relativa a un altro nodo nel paragrafo.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Inserisce la seconda sequenza nel paragrafo prima della sequenza iniziale.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Inserisce la terza esecuzione dopo l'esecuzione iniziale.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Inserisce la prima esecuzione all'inizio della raccolta di nodi figlio del paragrafo.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Possiamo modificare il contenuto della corsa modificando ed eliminando i nodi figlio esistenti.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Guarda anche

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../compositenode/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
