---
title: NodeImporter
second_title: Aspose.Words für .NET-API-Referenz
description: Initialisiert eine neue Instanz vonNodeImporteraspose.words/nodeimporter/ Klasse.
type: docs
weight: 10
url: /de/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Initialisiert eine neue Instanz von[`NodeImporter`](../) Klasse.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | DocumentBase | Das Quelldokument. |
| dstDoc | DocumentBase | Das Zieldokument, das der Besitzer importierter Knoten sein wird. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |

### Beispiele

Zeigt, wie Sie den Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument einfügen.

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
/// Fügt den Inhalt eines Dokuments nach dem angegebenen Knoten ein.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Alle Knoten auf Blockebene im Körper des Abschnitts durchlaufen,
        // Dann klonen und fügen Sie jeden Knoten ein, der nicht der letzte leere Absatz eines Abschnitts ist.
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

### Siehe auch

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* namensraum [Aspose.Words](../../nodeimporter/)
* Montage [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Initialisiert eine neue Instanz von[`NodeImporter`](../) Klasse.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | DocumentBase | Das Quelldokument. |
| dstDoc | DocumentBase | Das Zieldokument, das der Besitzer importierter Knoten sein wird. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |
| importFormatOptions | ImportFormatOptions | Gibt verschiedene Optionen zum Formatieren importierter Knoten an. |

### Beispiele

Zeigt, wie ein Konflikt beim Importieren von Dokumenten mit Listen mit derselben Listendefinitions-ID behoben wird.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true", um eine andere Listendefinitions-ID anzuwenden
// zu identischen Stilen, da Aspose.Words sie in Zieldokumente importiert.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Zeigt, wie Konflikte bei der Listennummerierung in Quell- und Zieldokumenten behoben werden.

```csharp
// Öffnen Sie ein Dokument mit einem benutzerdefinierten Listennummerierungsschema und klonen Sie es dann.
// Da beide dasselbe Nummerierungsformat haben, kollidieren die Formate, wenn wir ein Dokument in das andere importieren.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Wenn wir den Klon des Dokuments in das Original importieren und dann anhängen,
// dann werden die beiden Listen mit demselben Listenformat zusammengeführt.
// Wenn wir das "KeepSourceNumbering"-Flag auf "false" setzen, wird die Liste aus dem Dokument geklont
// die wir an das Original anhängen, wird die Nummerierung der Liste übernehmen, an die wir sie anhängen.
// Dadurch werden die beiden Listen effektiv zu einer zusammengeführt.
// Wenn wir das Flag "KeepSourceNumbering" auf "true" setzen, wird das Dokument geklont
// Die Liste behält ihre ursprüngliche Nummerierung bei, sodass die beiden Listen als separate Listen erscheinen. 
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

### Siehe auch

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* namensraum [Aspose.Words](../../nodeimporter/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
