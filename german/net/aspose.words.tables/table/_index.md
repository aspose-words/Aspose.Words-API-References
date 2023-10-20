---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words für .NET
description: Aspose.Words.Tables.Table klas. Stellt eine Tabelle in einem WordDokument dar in C#.
type: docs
weight: 6340
url: /de/net/aspose.words.tables/table/
---
## Table class

Stellt eine Tabelle in einem Word-Dokument dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Tabellen](https://docs.aspose.com/words/net/working-with-tables/) Dokumentationsartikel.

```csharp
public class Table : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initialisiert eine neue Instanz von`Table` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Ruft die durch die Tabelleneigenschaften angegebene absolute horizontale schwebende Tabellenposition in Punkten ab oder legt diese fest. Der Standardwert ist 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Ruft die durch die Tabelleneigenschaften angegebene absolute vertikale schwebende Tabellenposition in Punkten ab oder legt diese fest. Der Standardwert ist 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Gibt an, wie eine Inline-Tabelle im Dokument ausgerichtet wird. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Ermöglicht Microsoft Word und Aspose.Words, die Größe von Zellen in einer Tabelle automatisch an ihren Inhalt anzupassen. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Ruft die Option „Abstand zwischen Zellen zulassen“ ab oder legt diese fest. |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Ruft ab, ob eine schwebende Tabelle zulassen soll, dass andere schwebende Objekte im Dokument ihre Grenzen überlappen, wenn sie angezeigt werden. Der Standardwert ist`WAHR` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Ruft ab oder legt fest, ob es sich um eine von rechts nach links verlaufende Tabelle handelt. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Ruft den Abstand (in Punkten) ab, der unterhalb des Zellinhalts hinzugefügt werden soll, oder legt diesen fest. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Ruft den Abstand (in Punkten) zwischen den Zellen ab oder legt diesen fest. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Ruft die Beschreibung dieser Tabelle ab oder legt sie fest. Bietet eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Ruft den Abstand zwischen der Tabellenunterseite und dem umgebenden Text in Punkten ab oder legt diesen fest. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Ruft den Abstand zwischen der linken Tabelle und dem umgebenden Text in Punkten ab oder legt diesen fest. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Ruft den Abstand zwischen der rechten Tabellenseite und dem umgebenden Text in Punkten ab oder legt diesen fest. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Ruft den Abstand zwischen der Tischplatte und dem umgebenden Text in Punkten ab oder legt diesen fest. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Gibt den ersten zurück[`Row`](../row/) Knoten in der Tabelle. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt zurück`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Ruft das Basisobjekt ab, aus dem die horizontale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert istColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Gibt den letzten zurück[`Row`](../row/) Knoten in der Tabelle. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Ruft den Wert ab, der den linken Einzug der Tabelle darstellt, oder legt diesen fest. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Ruft den Abstand (in Punkten) ab, der links vom Zellinhalt hinzugefügt werden soll, oder legt diesen fest. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | Gibt zurückTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft das unmittelbare übergeordnete Element dieses Knotens ab. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Ruft die bevorzugte Tabellenbreite ab oder legt diese fest. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorangeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück[`Range`](../../aspose.words/range/) Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Ruft die relative horizontale Ausrichtung der schwebenden Tabelle ab oder legt sie fest. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Ruft die relative vertikale Ausrichtung der schwebenden Tabelle ab oder legt diese fest. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Ruft die Menge an Platz (in Punkten) ab, die rechts vom Inhalt der Zellen hinzugefügt werden soll, oder legt diese fest. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Bietet typisierten Zugriff auf die Zeilen der Tabelle. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Ruft den auf diese Tabelle angewendeten Tabellenstil ab oder legt diesen fest. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Ruft die vom Gebietsschema unabhängige Stilkennung des auf diese Tabelle angewendeten Tabellenstils ab oder legt diesen fest. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Ruft den Namen des Tabellenstils ab, der auf diese Tabelle angewendet wird, oder legt diesen fest. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Ruft Bitflags ab oder setzt diese, die angeben, wie ein Tabellenstil auf diese Tabelle angewendet wird. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Ruft ab oder legt fest[`TextWrapping`](./textwrapping/) für Tabelle. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Ruft den Titel dieser Tabelle ab oder legt ihn fest. Bietet eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Ruft die Menge an Platz (in Punkten) ab, die über dem Inhalt von Zellen hinzugefügt werden soll, oder legt diese fest. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Ruft das Basisobjekt ab, aus dem die vertikale Positionierung der schwebenden Tabelle berechnet werden soll. Der Standardwert istMargin . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Ändert die Größe der Tabelle und der Zellen entsprechend dem angegebenen automatischen Anpassungsverhalten. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Entfernt alle Tabellen- und Zellenränder dieser Tabelle. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Entfernt alle Schattierungen auf der Tabelle. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Konvertiert horizontal um die Breite verbundene Zellen in um zusammengeführte Zellen[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Wenn die Tabelle keine Zeilen enthält, wird eine erstellt und angehängt[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung untergeordneter Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration jedes Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/)Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten aus[`Node`](../../aspose.words/node/) das entspricht dem XPath-Ausdruck. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Setzt den angegebenen Tabellenrand auf den angegebenen Linienstil, die angegebene Breite und die angegebene Farbe. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Setzt alle Tabellenränder auf den angegebenen Linienstil, die angegebene Breite und die angegebene Farbe. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Setzt die Schattierung auf die angegebenen Werte für die gesamte Tabelle. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens mit den angegebenen Speicheroptionen in einen String. |

## Bemerkungen

`Table`ist ein Knoten auf Blockebene und kann ein untergeordnetes Element von abgeleiteten Klassen sein[`Story`](../../aspose.words/story/) or [`InlineStory`](../../aspose.words/inlinestory/).

`Table` kann eine oder mehrere enthalten[`Row`](../row/) Knoten.

Eine minimal gültige Tabelle muss mindestens eine haben[`Row`](../row/).

## Beispiele

Zeigt, wie eine Tabelle erstellt wird.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die möglicherweise Absätze enthalten
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Der Aufruf der Methode „EnsureMinimum“ für eine Tabelle stellt dies sicher
// Die Tabelle enthält mindestens eine Zeile, eine Zelle und einen Absatz.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Text zum ersten Aufruf in der ersten Zeile der Tabelle hinzufügen.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Zeigt, wie alle Tabellen im Dokument durchlaufen und der Inhalt jeder Zelle gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Wir können die Methode „ToArray“ für eine Zeilensammlung verwenden, um sie in ein Array zu klonen.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Wir können die Methode „ToArray“ für eine Zellsammlung verwenden, um sie in ein Array zu klonen.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

Zeigt, wie eine formatierte 2x2-Tabelle erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Beim Erstellen der Tabelle wendet der Document Builder seine aktuellen RowFormat/CellFormat-Eigenschaftswerte an
// zur aktuellen Zeile/Zelle, in der sich der Cursor befindet, und zu allen neuen Zeilen/Zellen, während sie erstellt werden.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Zuvor hinzugefügte Zeilen und Zellen werden von Änderungen an der Formatierung des Builders nicht rückwirkend beeinflusst.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Zeigt, wie man eine verschachtelte Tabelle erstellt, ohne einen Document Builder zu verwenden.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Erstellen Sie die äußere Tabelle mit drei Zeilen und vier Spalten und fügen Sie sie dann dem Dokument hinzu.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Erstelle eine weitere Tabelle mit zwei Zeilen und zwei Spalten und füge sie dann in die erste Zelle der ersten Tabelle ein.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Erstellt eine neue Tabelle im Dokument mit den angegebenen Abmessungen und Text in jeder Zelle.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Mit den Eigenschaften „Title“ und „Description“ können Sie Ihrer Tabelle einen Titel bzw. eine Beschreibung hinzufügen.
    // Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    // Diese Eigenschaften sind für ISO/IEC 29500-konforme .docx-Dokumente von Bedeutung (siehe die OoxmlCompliance-Klasse).
    // Wenn wir das Dokument in Formaten vor ISO/IEC 29500 speichern, ignoriert Microsoft Word diese Eigenschaften.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode/)
* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
