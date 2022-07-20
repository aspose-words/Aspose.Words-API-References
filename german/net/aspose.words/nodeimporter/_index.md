---
title: NodeImporter
second_title: Aspose.Words für .NET-API-Referenz
description: Ermöglicht den effizienten wiederholten Import von Knoten von einem Dokument in ein anderes.
type: docs
weight: 3970
url: /de/net/aspose.words/nodeimporter/
---
## NodeImporter class

Ermöglicht den effizienten wiederholten Import von Knoten von einem Dokument in ein anderes.

```csharp
public class NodeImporter
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [NodeImporter](nodeimporter#constructor)(DocumentBase, DocumentBase, ImportFormatMode) | Initialisiert eine neue Instanz von[`NodeImporter`](../nodeimporter) Klasse. |
| [NodeImporter](nodeimporter#constructor_1)(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) | Initialisiert eine neue Instanz von[`NodeImporter`](../nodeimporter) Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode)(Node, bool) | Importiert einen Knoten von einem Dokument in ein anderes. |

### Bemerkungen

Aspose.Words bietet Funktionen zum einfachen Kopieren und Verschieben von fragments zwischen Microsoft Word-Dokumenten. Dies wird als "Importieren von Knoten" bezeichnet. Bevor Sie ein Fragment aus einem Dokument in ein anderes einfügen können, müssen Sie es "importieren". Beim Importieren wird ein tiefer Klon des ursprünglichen Knotens erstellt, der in das Zieldokument eingefügt werden kann.

Der einfachste Weg, einen Knoten zu importieren, ist die Verwendung der[`ImportNode`](../documentbase/importnode) method bereitgestellt von der[`DocumentBase`](../documentbase) Objekt.

Wenn Sie Knoten jedoch mehrmals von einem Dokument in ein anderes importieren müssen, ist es besser, die zu verwenden[`NodeImporter`](../nodeimporter) Klasse. Das[`NodeImporter`](../nodeimporter) Die Klasse ermöglicht es, die Anzahl der im Zieldokument erstellten Stile und Listen zu minimieren.

Das Kopieren oder Verschieben von Fragmenten von einem Microsoft Word-Dokument in ein anderes stellt eine Reihe technischer Herausforderungen für Aspose.Words dar. In einem Word-Dokument werden Stile und Listenformatierungen zentral gespeichert, getrennt vom Text des Dokuments. Die Absätze und Textläufe referenzieren die Stile lediglich durch interne eindeutige Kennungen.

Die Herausforderungen ergeben sich aus der Tatsache, dass Stile und Listen in verschiedenen Dokumenten unterschiedlich sind. Um beispielsweise einen Absatz, der mit dem Stil Überschrift 1 formatiert ist, von einem Dokument in ein anderes zu kopieren , müssen einige Dinge berücksichtigt werden: Entscheiden Sie, ob Sie das tun sollen Kopieren Sie die Überschrift 1-Formatvorlage aus dem Quelldokument in das Zieldokument, klonen Sie den Absatz, aktualisieren Sie den geklonten -Absatz so, dass er auf die richtige Überschrift 1-Formatvorlage im Zieldokument verweist. Wenn die Formatvorlage kopiert werden musste, alle Formatvorlagen, die sie enthält Verweise (basierend auf style und dem nächsten Absatzstil) sollten analysiert und möglicherweise auch kopiert werden usw. Ähnliche Probleme treten auf, wenn Aufzählungszeichen oder nummerierte Absätze kopiert werden, da Microsoft Word Listendefinitionen getrennt vom Text speichert.

Das[`NodeImporter`](../nodeimporter)class ist wie ein Kontext, der beim Import die "Übersetzungstabellen" hält. Es übersetzt korrekt zwischen Stilen und Listen in den Quell- und -Zieldokumenten.

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

* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
