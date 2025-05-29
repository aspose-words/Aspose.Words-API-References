---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.NodeType per identificare e gestire facilmente diversi tipi di nodi di documenti Word per un'elaborazione fluida dei documenti.
type: docs
weight: 4920
url: /it/net/aspose.words/nodetype/
---
## NodeType enumeration

Specifica il tipo di un nodo di documento Word.

```csharp
public enum NodeType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Any | `0` | Indica tutti i tipi di nodo. Permette di selezionare tutti i nodi figlio. |
| Document | `1` | UN[`Document`](../document/) oggetto che, in quanto radice dell'albero dei documenti, fornisce accesso all'intero documento Word. |
| Section | `2` | UN[`Section`](../section/) oggetto che corrisponde a una sezione di un documento Word. |
| Body | `3` | UN[`Body`](../body/) oggetto che contiene il testo principale di una sezione (testo principale della storia). |
| HeaderFooter | `4` | UN[`HeaderFooter`](../headerfooter/) Oggetto che contiene il testo di una particolare intestazione o piè di pagina all'interno di una sezione. |
| Table | `5` | UN[`Table`](../../aspose.words.tables/table/) oggetto che rappresenta una tabella in un documento Word. |
| Row | `6` | Una fila di tavoli. |
| Cell | `7` | Una cella di una riga di una tabella. |
| Paragraph | `8` | Un paragrafo di testo. |
| BookmarkStart | `9` | L'inizio di un segnalibro. |
| BookmarkEnd | `10` | Estremità di un segnalibro. |
| EditableRangeStart | `11` | Inizio di un intervallo modificabile. |
| EditableRangeEnd | `12` | Fine di un intervallo modificabile. |
| MoveFromRangeStart | `13` | L'inizio di un intervallo MoveFrom. |
| MoveFromRangeEnd | `14` | Fine di un intervallo MoveFrom. |
| MoveToRangeStart | `15` | L'inizio di un intervallo MoveTo. |
| MoveToRangeEnd | `16` | Fine di un intervallo MoveTo. |
| GroupShape | `17` | Un gruppo di forme, immagini, oggetti OLE o altre forme di gruppo. |
| Shape | `18` | Un oggetto di disegno, ad esempio una forma di OfficeArt, un'immagine o un oggetto OLE. |
| Comment | `19` | Un commento in un documento Word. |
| Footnote | `20` | Una nota a piè di pagina o una nota di chiusura in un documento Word. |
| Run | `21` | Una sequenza di testo. |
| FieldStart | `22` | Carattere speciale che designa l'inizio di un campo Word. |
| FieldSeparator | `23` | Carattere speciale che separa il codice del campo dal risultato del campo. |
| FieldEnd | `24` | Carattere speciale che indica la fine di un campo Word. |
| FormField | `25` | Un campo modulo. |
| SpecialChar | `26` | Un carattere speciale che non rientra nei tipi di caratteri speciali più specifici. |
| SmartTag | `27` | Un tag intelligente attorno a una o più strutture inline (esercitazioni, immagini, campi, ecc.) all'interno di un paragrafo |
| StructuredDocumentTag | `28` | Permette di definire informazioni specifiche del cliente e le relative modalità di presentazione. |
| StructuredDocumentTagRangeStart | `29` | Un inizio di**a distanza** tag di documento strutturato che accetta contenuti multi-sezione. |
| StructuredDocumentTagRangeEnd | `30` | Una fine di**a distanza** tag di documento strutturato che accetta contenuti multi-sezione. |
| GlossaryDocument | `31` | Un documento di glossario all'interno del documento principale. |
| BuildingBlock | `32` | Un elemento costitutivo all'interno di un documento di glossario (ad esempio una voce di documento di glossario). |
| CommentRangeStart | `33` | Un nodo marcatore che rappresenta l'inizio di un intervallo commentato. |
| CommentRangeEnd | `34` | Un nodo marcatore che rappresenta la fine di un intervallo commentato. |
| OfficeMath | `35` | Un oggetto di Office Math. Può essere un'equazione, una funzione, una matrice o uno qualsiasi degli altri oggetti matematici. Può essere una raccolta di oggetti matematici e può contenere anche oggetti non matematici, come sequenze di testo. |
| SubDocument | `36` | Un nodo di sottodocumento che è un collegamento a un altro documento. |
| System | `37` | Riservato per uso interno da Aspose.Words. |
| Null | `38` | Riservato per uso interno da Aspose.Words. |

## Esempi

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
