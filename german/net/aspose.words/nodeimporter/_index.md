---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words für .NET
description: Aspose.Words.NodeImporter klas. Ermöglicht die effiziente Durchführung wiederholter Importe von Knoten von einem Dokument in ein anderes in C#.
type: docs
weight: 4210
url: /de/net/aspose.words/nodeimporter/
---
## NodeImporter class

Ermöglicht die effiziente Durchführung wiederholter Importe von Knoten von einem Dokument in ein anderes.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class NodeImporter
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Initialisiert eine neue Instanz von`NodeImporter` Klasse. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Initialisiert eine neue Instanz von`NodeImporter` Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Importiert einen Knoten aus einem Dokument in ein anderes. |

## Bemerkungen

Aspose.Words bietet Funktionen zum einfachen Kopieren und Verschieben von Fragmenten zwischen Microsoft Word-Dokumenten. Dies wird als „Importieren von Knoten“ bezeichnet. Bevor Sie ein Fragment aus einem Dokument in ein anderes einfügen können, müssen Sie es „importieren“. Beim Importieren wird ein tiefer Klon des ursprünglichen Knotens erstellt, der in das Zieldokument eingefügt werden kann.

Der einfachste Weg, einen Knoten zu importieren, ist die Verwendung von[`ImportNode`](../documentbase/importnode/) method bereitgestellt von der[`DocumentBase`](../documentbase/) Objekt.

Wenn Sie jedoch mehrmals Knoten von einem Dokument in ein anderes importieren müssen, ist es besser, die zu verwenden`NodeImporter` Klasse. Der`NodeImporter` Mit der Klasse kann die Anzahl der im Zieldokument erstellten Stile und Listen minimiert werden.

Das Kopieren oder Verschieben von Fragmenten von einem Microsoft Word-Dokument in ein anderes stellt Aspose.Words vor unzählige technische Herausforderungen. In einem Word-Dokument werden Stile und Listenformatierung zentral gespeichert, getrennt vom Text des Dokuments. Die Absätze und Textläufe verweisen lediglich auf die Stile durch interne eindeutige Bezeichner.

Die Herausforderungen ergeben sich aus der Tatsache, dass Stile und Listen in verschiedenen Dokumenten unterschiedlich sind. Um beispielsweise einen Absatz, der mit dem Stil „Überschrift 1“ formatiert ist, von einem Dokument in ein anderes zu kopieren, müssen eine Reihe von Dingen berücksichtigt werden: Entscheiden Sie, ob dies geschehen soll Kopieren Sie den Stil „Überschrift 1“ aus dem Quelldokument in das Zieldokument, klonen Sie den Absatz, aktualisieren Sie den geklonten Absatz, sodass er auf den korrekten Stil „Überschrift 1“ im Zieldokument verweist. Wenn der Stil kopiert werden musste, alle darin enthaltenen Stile Referenzen (basierend auf style und dem nächsten Absatzstil) sollten analysiert und möglicherweise auch kopiert werden usw. Ähnliche Probleme treten beim Kopieren von Aufzählungszeichen oder nummerierten Absätzen auf, da Microsoft Word Listendefinitionen getrennt vom Text speichert.

Der`NodeImporter`Die Klasse ist wie ein Kontext, der die „Übersetzungstabellen“ während des Imports enthält. Es übersetzt korrekt zwischen Stilen und Listen in den Quell- und Zieldokumenten.

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

        // Alle Knoten auf Blockebene im Hauptteil des Abschnitts durchlaufen,
        // dann jeden Knoten klonen und einfügen, der nicht der letzte leere Absatz eines Abschnitts ist.
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
