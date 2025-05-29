---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.NodeType, um verschiedene Word-Dokumentknotentypen für eine nahtlose Dokumentverarbeitung einfach zu identifizieren und zu verwalten.
type: docs
weight: 4920
url: /de/net/aspose.words/nodetype/
---
## NodeType enumeration

Gibt den Typ eines Word-Dokumentknotens an.

```csharp
public enum NodeType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Any | `0` | Zeigt alle Knotentypen an. Ermöglicht die Auswahl aller untergeordneten Knoten. |
| Document | `1` | A[`Document`](../document/) Objekt, das als Wurzel des Dokumentbaums Zugriff auf das gesamte Word-Dokument bietet. |
| Section | `2` | A[`Section`](../section/) Objekt, das einem Abschnitt in einem Word-Dokument entspricht. |
| Body | `3` | A[`Body`](../body/) Objekt, das den Haupttext eines Abschnitts enthält (Haupttextgeschichte). |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter/) Objekt, das Text einer bestimmten Kopf- oder Fußzeile innerhalb eines Abschnitts enthält. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table/) Objekt, das eine Tabelle in einem Word-Dokument darstellt. |
| Row | `6` | Eine Zeile einer Tabelle. |
| Cell | `7` | Eine Zelle einer Tabellenzeile. |
| Paragraph | `8` | Ein Textabsatz. |
| BookmarkStart | `9` | Der Anfang eines Lesezeichenmarkers. |
| BookmarkEnd | `10` | Das Ende eines Lesezeichenmarkers. |
| EditableRangeStart | `11` | Der Anfang eines bearbeitbaren Bereichs. |
| EditableRangeEnd | `12` | Das Ende eines bearbeitbaren Bereichs. |
| MoveFromRangeStart | `13` | Der Anfang eines MoveFrom-Bereichs. |
| MoveFromRangeEnd | `14` | Das Ende eines MoveFrom-Bereichs. |
| MoveToRangeStart | `15` | Der Anfang eines MoveTo-Bereichs. |
| MoveToRangeEnd | `16` | Das Ende eines MoveTo-Bereichs. |
| GroupShape | `17` | Eine Gruppe von Formen, Bildern, OLE-Objekten oder anderen Gruppenformen. |
| Shape | `18` | Ein Zeichenobjekt, beispielsweise eine OfficeArt-Form, ein Bild oder ein OLE-Objekt. |
| Comment | `19` | Ein Kommentar in einem Word-Dokument. |
| Footnote | `20` | Eine Fußnote oder Endnote in einem Word-Dokument. |
| Run | `21` | Ein Textlauf. |
| FieldStart | `22` | Ein Sonderzeichen, das den Anfang eines Wortfelds kennzeichnet. |
| FieldSeparator | `23` | Ein Sonderzeichen, das den Feldcode vom Feldergebnis trennt. |
| FieldEnd | `24` | Ein Sonderzeichen, das das Ende eines Wortfelds kennzeichnet. |
| FormField | `25` | Ein Formularfeld. |
| SpecialChar | `26` | Ein Sonderzeichen, das nicht zu den spezifischeren Sonderzeichentypen gehört. |
| SmartTag | `27` | Ein Smarttag um eine oder mehrere Inline-Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes |
| StructuredDocumentTag | `28` | Ermöglicht die Definition kundenspezifischer Informationen und deren Darstellungsformen. |
| StructuredDocumentTagRangeStart | `29` | Ein Anfang von**reichte** strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. |
| StructuredDocumentTagRangeEnd | `30` | Ein Ende von**reichte** strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. |
| GlossaryDocument | `31` | Ein Glossardokument innerhalb des Hauptdokuments. |
| BuildingBlock | `32` | Ein Baustein innerhalb eines Glossardokuments (z. B. Glossardokumenteintrag). |
| CommentRangeStart | `33` | Ein Markierungsknoten, der den Anfang eines kommentierten Bereichs darstellt. |
| CommentRangeEnd | `34` | Ein Markierungsknoten, der das Ende eines kommentierten Bereichs darstellt. |
| OfficeMath | `35` | Ein Office Math-Objekt. Kann eine Gleichung, Funktion, Matrix oder eines anderer mathematischer Objekte sein. Kann eine Sammlung mathematischer Objekte sein und auch einige nicht-mathematische Objekte wie Textläufe enthalten. |
| SubDocument | `36` | Ein Unterdokumentknoten, der eine Verknüpfung zu einem anderen Dokument darstellt. |
| System | `37` | Für die interne Verwendung durch Aspose.Words reserviert. |
| Null | `38` | Für die interne Verwendung durch Aspose.Words reserviert. |

## Beispiele

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die „CustomNodeId“ nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durchlaufen Sie die Sammlung der unmittelbar untergeordneten Elemente des Absatzes.
// und drucke alle Läufe oder Formen aus, die wir darin finden.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
