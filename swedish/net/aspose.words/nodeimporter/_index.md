---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words för .NET
description: Överför dokumentnoder enkelt med Aspose.Words.NodeImporter. Effektivisera ditt arbetsflöde och förbättra dokumenthanteringens effektivitet idag!
type: docs
weight: 4900
url: /sv/net/aspose.words/nodeimporter/
---
## NodeImporter class

Möjliggör effektiv upprepad import av noder från ett dokument till ett annat.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class NodeImporter
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Initierar en ny instans av`NodeImporter` klass. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Initierar en ny instans av`NodeImporter` klass. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Importerar en nod från ett dokument till ett annat. |

## Anmärkningar

Aspose.Words tillhandahåller funktioner för enkel kopiering och flyttning av fragment mellan Microsoft Word-dokument. Detta kallas "import av noder". Innan du kan infoga ett fragment från ett dokument till ett annat måste du "importera" det. Import skapar en djup klon av den ursprungliga noden, redo att infogas i destinationsdokumentet.

Det enklaste sättet att importera en nod är att använda[`ImportNode`](../documentbase/importnode/) metod tillhandahållen av[`DocumentBase`](../documentbase/) objekt.

Men när du behöver importera noder från ett dokument till ett annat flera gånger, är det bättre att använda`NodeImporter` klass. Den`NodeImporter` Klassen gör det möjligt att minimera antalet stilar och listor som skapas i destinationsdokumentet.

Att kopiera eller flytta fragment från ett Microsoft Word-dokument till ett annat innebär ett antal tekniska utmaningar för Aspose.Words. I ett Word-dokument lagras stilar och listformatering centralt, separat från dokumentets text. Styckena och textsekvenserna refererar endast till stilarna med interna unika identifierare.

Utmaningarna uppstår på grund av att formatmallar och listor skiljer sig åt i olika dokument. För att till exempel kopiera ett stycke formaterat med formatet Rubrik 1 från ett dokument till ett annat, måste ett antal saker beaktas: bestämma om formatet Rubrik 1 ska kopieras från källdokumentet till destinationsdokumentet, klona stycket, uppdatera det klonade stycket så att det refererar till rätt formatmall för Rubrik 1 i destinationsdokumentet. Om formatet måste kopieras bör alla formatmallar som det refererar till (baserat på formatmall och formatmallen för nästa stycke) analyseras och eventuellt kopieras också och så vidare. Liknande problem uppstår när man kopierar punktlistor eller numrerade stycken eftersom Microsoft Word lagrar listdefinitioner separat från text.

De`NodeImporter`Klassen är som ett sammanhang som innehåller "översättningstabellerna" under importen. Den översätter korrekt mellan stilar och listor i käll- och destinationsdokumenten.

## Exempel

Visar hur man infogar innehållet i ett dokument till ett bokmärke i ett annat dokument.

```csharp
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

        // Loopa igenom alla blocknivånoder i sektionens brödtext,
        // klona och infoga sedan varje nod som inte är det sista tomma stycket i ett avsnitt.
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
