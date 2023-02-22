---
title: NodeImporter.NodeImporter
second_title: Aspose.Words för .NET API Referens
description: NodeImporter byggare. Initierar en ny instans avNodeImporter class.
type: docs
weight: 10
url: /sv/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Initierar en ny instans av[`NodeImporter`](../) class.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | DocumentBase | Källdokumentet. |
| dstDoc | DocumentBase | Måldokumentet som kommer att vara ägare till importerade noder. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |

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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* namnutrymme [Aspose.Words](../../nodeimporter/)
* hopsättning [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Initierar en ny instans av[`NodeImporter`](../) class.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | DocumentBase | Källdokumentet. |
| dstDoc | DocumentBase | Måldokumentet som kommer att vara ägare till importerade noder. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |
| importFormatOptions | ImportFormatOptions | Anger olika alternativ för att formatera importerad nod. |

### Exempel

Visar hur man löser en konflikt när man importerar dokument som har listor med samma listdefinitionsidentifierare.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Ställ in egenskapen "KeepSourceNumbering" till "true" för att tillämpa ett annat listdefinitions-ID
// till identiska stilar som Aspose.Words importerar dem till måldokument.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Visar hur man löser listnumreringskrockar i käll- och måldokument.

```csharp
// Öppna ett dokument med ett anpassat listnumreringsschema och klona det sedan.
// Eftersom båda har samma numreringsformat kommer formaten att krocka om vi importerar ett dokument till det andra.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// När vi importerar dokumentets klon till originalet och sedan lägger till det,
// då kommer de två listorna med samma listformat att förenas.
// Om vi ställer in "KeepSourceNumbering"-flaggan till "false", kommer listan från dokumentklonen
// som vi lägger till originalet kommer att fortsätta numreringen av listan vi lägger till den.
// Detta kommer effektivt att slå samman de två listorna till en.
// Om vi ställer in "KeepSourceNumbering"-flaggan till "true", kommer dokumentklonen
// list kommer att bevara sin ursprungliga numrering, vilket gör att de två listorna visas som separata listor. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Se även

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* namnutrymme [Aspose.Words](../../nodeimporter/)
* hopsättning [Aspose.Words](../../../)


