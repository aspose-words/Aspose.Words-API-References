---
title: NodeImporter
second_title: Aspose.Words för .NET API Referens
description: Gör det möjligt att effektivt utföra upprepad import av noder från ett dokument till ett annat.
type: docs
weight: 3970
url: /sv/net/aspose.words/nodeimporter/
---
## NodeImporter class

Gör det möjligt att effektivt utföra upprepad import av noder från ett dokument till ett annat.

```csharp
public class NodeImporter
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Initierar en ny instans av`NodeImporter` class. |
| [NodeImporter](nodeimporter/#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Initierar en ny instans av`NodeImporter` class. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(Node, bool) | Importerar en nod från ett dokument till ett annat. |

### Anmärkningar

Aspose.Words tillhandahåller funktionalitet för enkel kopiering och flyttning av fragments mellan Microsoft Word-dokument. Detta är känt som "importerande noder". Innan du kan infoga ett fragment från ett dokument till ett annat måste du "importera" det. Import skapar en djup klon av den ursprungliga noden, redo att infogas i destinationsdokumentet.

Det enklaste sättet att importera en nod är att använda[`ImportNode`](../documentbase/importnode/) method tillhandahålls av[`DocumentBase`](../documentbase/) objekt.

Men när du behöver importera noder från ett dokument till ett annat flera gånger, är det bättre att använda`NodeImporter` klass. De`NodeImporter` class gör det möjligt att minimera antalet stilar och listor som skapas i måldokumentet.

Att kopiera eller flytta fragment från ett Microsoft Word-dokument till ett annat innebär ett antal tekniska utmaningar för Aspose.Words. I ett Word-dokument lagras stilar och listformatering centralt, separat från dokumentets text. Paragraferna och textserierna refererar bara till stilarna med interna unika identifierare.

Utmaningarna beror på att stilar och listor är olika i olika dokument. För att till exempel kopiera ett stycke formaterat med stilen Rubrik 1 från ett dokument till ett annat måste ta hänsyn till ett antal saker: besluta om du ska kopiera stilen Rubrik 1 från källdokumentet till måldokumentet, klona stycket, uppdatera stycket cloned så att det hänvisar till rätt rubrik 1-format i måldokumentet. Om stilen var tvungen att kopieras, alla stilar som den referenser (baserat på stil och nästa styckestil) bör analyseras och eventuellt kopieras också och så vidare. Liknande problem finns vid kopiering av punkt- eller numrerade stycken eftersom Microsoft Word lagrar listdefinitioner separat från text.

De`NodeImporter`klass är som ett sammanhang, som innehåller "översättningstabellerna" under importen. Den översätter korrekt mellan stilar och listor i käll- och -destinationsdokumenten.

### Exempel

Visar hur man infogar innehållet i ett dokument till ett bokmärke i ett annat dokument.

```csharp
[Test]
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Infogar innehållet i ett dokument efter den angivna noden.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Slinga igenom alla noder på blocknivå i sektionens kropp,
        // klona sedan och infoga varje nod som inte är det sista tomma stycket i ett avsnitt.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
