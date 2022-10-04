---
title: NodeType
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt den Typ eines WordDokumentknotens an.
type: docs
weight: 3990
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
| Any | `0` | Zeigt alle Knotentypen an. Ermöglicht die Auswahl aller Kinder. |
| Document | `1` | EIN[`Document`](../document/) Objekt, das als Wurzel des Dokumentbaums Zugriff auf das gesamte Word-Dokument bietet. |
| Section | `2` | EIN[`Section`](../section/) Objekt, das einem Abschnitt in einem Word-Dokument entspricht. |
| Body | `3` | EIN[`Body`](../body/) Objekt, das den Haupttext eines Abschnitts enthält (Haupttextstory). |
| HeaderFooter | `4` | EIN[`HeaderFooter`](../headerfooter/) Objekt, das Text einer bestimmten Kopf- oder Fußzeile innerhalb eines Abschnitts enthält. |
| Table | `5` | EIN[`Table`](../../aspose.words.tables/table/) Objekt, das eine Tabelle in einem Word-Dokument darstellt. |
| Row | `6` | Eine Reihe einer Tabelle. |
| Cell | `7` | Eine Zelle einer Tabellenzeile. |
| Paragraph | `8` | Ein Textabschnitt. |
| BookmarkStart | `9` | Ein Anfang einer Lesezeichenmarkierung. |
| BookmarkEnd | `10` | Ein Ende einer Lesezeichenmarkierung. |
| EditableRangeStart | `11` | Ein Anfang eines bearbeitbaren Bereichs. |
| EditableRangeEnd | `12` | Ein Ende eines bearbeitbaren Bereichs. |
| MoveFromRangeStart | `13` | Ein Beginn eines MoveFrom-Bereichs. |
| MoveFromRangeEnd | `14` | Ein Ende eines MoveFrom-Bereichs. |
| MoveToRangeStart | `15` | Ein Anfang eines MoveTo-Bereichs. |
| MoveToRangeEnd | `16` | Ein Ende eines MoveTo-Bereichs. |
| GroupShape | `17` | Eine Gruppe von Formen, Bildern, OLE-Objekten oder anderen Gruppenformen. |
| Shape | `18` | Ein Zeichnungsobjekt, z. B. eine OfficeArt-Form, ein Bild oder ein OLE-Objekt. |
| Comment | `19` | Ein Kommentar in einem Word-Dokument. |
| Footnote | `20` | Eine Fußnote oder Endnote in einem Word-Dokument. |
| Run | `21` | Eine Textreihe. |
| FieldStart | `22` | Ein Sonderzeichen, das den Anfang eines Wortfelds kennzeichnet. |
| FieldSeparator | `23` | Ein Sonderzeichen, das den Feldcode vom Feldergebnis trennt. |
| FieldEnd | `24` | Ein Sonderzeichen, das das Ende eines Word-Felds kennzeichnet. |
| FormField | `25` | Ein Formularfeld. |
| SpecialChar | `26` | Ein Sonderzeichen, das nicht zu den spezifischeren Sonderzeichentypen gehört. |
| SmartTag | `27` | Ein Smart Tag um eine oder mehrere Inline-Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes |
| StructuredDocumentTag | `28` | Ermöglicht die Definition kundenspezifischer Informationen und deren Darstellung. |
| StructuredDocumentTagRangeStart | `29` | Ein Anfang von **reichte** strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. |
| StructuredDocumentTagRangeEnd | `30` | Ein Ende von **reichte** strukturiertes Dokument-Tag, das Inhalte mit mehreren Abschnitten akzeptiert. |
| GlossaryDocument | `31` | Ein Glossardokument innerhalb des Hauptdokuments. |
| BuildingBlock | `32` | Ein Baustein innerhalb eines Glossardokuments (zB Glossardokumenteintrag). |
| CommentRangeStart | `33` | Ein Markierungsknoten, der den Beginn eines kommentierten Bereichs darstellt. |
| CommentRangeEnd | `34` | Ein Markierungsknoten, der das Ende eines kommentierten Bereichs darstellt. |
| OfficeMath | `35` | Ein Office Math-Objekt. Kann eine Gleichung, Funktion, Matrix oder eines von anderen mathematischen Objekten sein. Kann eine Sammlung von mathematischen Objekten sein und kann auch einige nicht-mathematische Objekte wie Textfolgen enthalten. |
| SubDocument | `36` | Ein untergeordneter Dokumentknoten, der eine Verknüpfung zu einem anderen Dokument darstellt. |
| System | `37` | Reserviert für die interne Verwendung durch Aspose.Words. |
| Null | `38` | Reserviert für die interne Verwendung durch Aspose.Words. |

### Beispiele

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durch die Sammlung der unmittelbaren Kinder des Absatzes iterieren,
// und drucken Sie alle Läufe oder Formen, die wir darin finden.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
