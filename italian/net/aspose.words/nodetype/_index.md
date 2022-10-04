---
title: NodeType
second_title: Aspose.Words per .NET API Reference
description: Specifica il tipo di nodo di un documento di Word.
type: docs
weight: 3990
url: /it/net/aspose.words/nodetype/
---
## NodeType enumeration

Specifica il tipo di nodo di un documento di Word.

```csharp
public enum NodeType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Any | `0` | Indica tutti i tipi di nodo. Consente di selezionare tutti i bambini. |
| Document | `1` | UN[`Document`](../document/) oggetto che, come radice dell'albero del documento, fornisce l'accesso all'intero documento di Word. |
| Section | `2` | UN[`Section`](../section/) oggetto che corrisponde a una sezione in un documento di Word. |
| Body | `3` | UN[`Body`](../body/) oggetto che contiene il testo principale di una sezione (storia di testo principale). |
| HeaderFooter | `4` | UN[`HeaderFooter`](../headerfooter/) oggetto che contiene il testo di una particolare intestazione o piè di pagina all'interno di una sezione. |
| Table | `5` | UN[`Table`](../../aspose.words.tables/table/) oggetto che rappresenta una tabella in un documento di Word. |
| Row | `6` | Una riga di una tabella. |
| Cell | `7` | Una cella di una riga di tabella. |
| Paragraph | `8` | Un paragrafo di testo. |
| BookmarkStart | `9` | L'inizio di un segnalibro. |
| BookmarkEnd | `10` | Un'estremità di un segnalibro. |
| EditableRangeStart | `11` | Un inizio di un intervallo modificabile. |
| EditableRangeEnd | `12` | Fine di un intervallo modificabile. |
| MoveFromRangeStart | `13` | Un inizio di un intervallo MoveFrom. |
| MoveFromRangeEnd | `14` | La fine di un intervallo MoveFrom. |
| MoveToRangeStart | `15` | Un inizio di un intervallo MoveTo. |
| MoveToRangeEnd | `16` | Fine di un intervallo MoveTo. |
| GroupShape | `17` | Un gruppo di forme, immagini, oggetti OLE o altre forme di gruppo. |
| Shape | `18` | Un oggetto di disegno, ad esempio una forma OfficeArt, un'immagine o un oggetto OLE. |
| Comment | `19` | Un commento in un documento di Word. |
| Footnote | `20` | Una nota a piè di pagina o una nota di chiusura in un documento di Word. |
| Run | `21` | Una corsa di testo. |
| FieldStart | `22` | Un carattere speciale che designa l'inizio di un campo Word. |
| FieldSeparator | `23` | Un carattere speciale che separa il codice del campo dal risultato del campo. |
| FieldEnd | `24` | Un carattere speciale che indica la fine di un campo Word. |
| FormField | `25` | Un campo modulo. |
| SpecialChar | `26` | Un carattere speciale che non è uno dei tipi di caratteri speciali più specifici. |
| SmartTag | `27` | Uno smart tag attorno a una o più strutture inline (corse, immagini, campi, ecc.) all'interno di un paragrafo |
| StructuredDocumentTag | `28` | Consente di definire le informazioni specifiche del cliente e le relative modalità di presentazione. |
| StructuredDocumentTagRangeStart | `29` | Un inizio di **a distanza** tag del documento strutturato che accetta contenuti multisezione. |
| StructuredDocumentTagRangeEnd | `30` | Una fine di **a distanza** tag del documento strutturato che accetta contenuti multisezione. |
| GlossaryDocument | `31` | Un documento glossario all'interno del documento principale. |
| BuildingBlock | `32` | Un elemento costitutivo all'interno di un documento del glossario (ad es. voce di un documento del glossario). |
| CommentRangeStart | `33` | Un nodo marker che rappresenta l'inizio di un intervallo commentato. |
| CommentRangeEnd | `34` | Un nodo marker che rappresenta la fine di un intervallo commentato. |
| OfficeMath | `35` | Un oggetto Office Math. Può essere un'equazione, una funzione, una matrice o uno di altri oggetti matematici. Può essere una raccolta di oggetti matematici e può anche contenere alcuni oggetti non matematici come sequenze di testo. |
| SubDocument | `36` | Un nodo di documento secondario che è un collegamento a un altro documento. |
| System | `37` | Riservato per uso interno da Aspose.Words. |
| Null | `38` | Riservato per uso interno da Aspose.Words. |

### Esempi

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
