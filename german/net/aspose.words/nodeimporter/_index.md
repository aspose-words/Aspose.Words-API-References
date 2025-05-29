---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words für .NET
description: Übertragen Sie mühelos Dokumentknoten mit Aspose.Words.NodeImporter. Optimieren Sie Ihren Workflow und steigern Sie die Effizienz Ihres Dokumentenmanagements!
type: docs
weight: 4900
url: /de/net/aspose.words/nodeimporter/
---
## NodeImporter class

Ermöglicht den effizienten wiederholten Import von Knoten von einem Dokument in ein anderes.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class NodeImporter
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Initialisiert eine neue Instanz des`NodeImporter` Klasse. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Initialisiert eine neue Instanz des`NodeImporter` Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Importiert einen Knoten aus einem Dokument in ein anderes. |

## Bemerkungen

Aspose.Words bietet Funktionen zum einfachen Kopieren und Verschieben von Fragmenten zwischen Microsoft Word-Dokumenten. Dies wird als „Importieren von Knoten“ bezeichnet. Bevor Sie ein Fragment aus einem Dokument in ein anderes einfügen können, müssen Sie es „importieren“. Beim Importieren wird ein vollständiger Klon des ursprünglichen Knotens erstellt, der in das Zieldokument eingefügt werden kann.

Der einfachste Weg, einen Knoten zu importieren, ist die Verwendung des[`ImportNode`](../documentbase/importnode/) method bereitgestellt durch[`DocumentBase`](../documentbase/) Objekt.

Wenn Sie jedoch Knoten mehrmals von einem Dokument in ein anderes importieren müssen, ist es besser, die`NodeImporter` Klasse. Die`NodeImporter` Mit der Klasse kann die Anzahl der im Zieldokument erstellten Stile und Listen minimiert werden.

Das Kopieren oder Verschieben von Fragmenten von einem Microsoft Word-Dokument in ein anderes stellt für Aspose.Words eine Reihe technischer Herausforderungen dar. In einem Word-Dokument werden Formatvorlagen und Listenformatierungen zentral und getrennt vom Text gespeichert. Absätze und Textabschnitte verweisen lediglich über interne eindeutige Kennungen auf die Formatvorlagen.

Die Herausforderungen ergeben sich aus der Tatsache, dass Stile und Listen in verschiedenen Dokumenten unterschiedlich sind. Um beispielsweise einen mit dem Stil „Überschrift 1“ formatierten Absatz von einem Dokument in ein anderes zu kopieren, müssen verschiedene Dinge berücksichtigt werden: Entscheiden Sie, ob der Stil „Überschrift 1“ vom Quelldokument in das Zieldokument kopiert werden soll, klonen Sie den Absatz, aktualisieren Sie den geklonten Absatz, sodass er im Zieldokument auf den richtigen Stil „Überschrift 1“ verweist. Wenn der Stil kopiert werden musste, sollten alle Stile, auf die er verweist (basierend auf Stil und Stil des nächsten Absatzes), analysiert und möglicherweise ebenfalls kopiert werden usw. Ähnliche Probleme treten beim Kopieren von Aufzählungs- oder nummerierten Absätzen auf, da Microsoft Word Listendefinitionen getrennt vom Text speichert.

Der`NodeImporter`Die Klasse ist wie ein Kontext, der die Übersetzungstabellen während des Imports enthält. Sie übersetzt korrekt zwischen Stilen und Listen in den Quell- und Zieldokumenten.

## Beispiele

Zeigt, wie der Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument eingefügt wird.

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
/// Fügt den Inhalt eines Dokuments nach dem angegebenen Knoten ein.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Durchlaufe alle Knoten auf Blockebene im Hauptteil des Abschnitts,
        // dann klonen und fügen Sie jeden Knoten ein, der nicht der letzte leere Absatz eines Abschnitts ist.
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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
