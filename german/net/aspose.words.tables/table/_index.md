---
title: Table
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt eine Tabelle in einem WordDokument dar.
type: docs
weight: 6040
url: /de/net/aspose.words.tables/table/
---
## Table class

Stellt eine Tabelle in einem Word-Dokument dar.

```csharp
public class Table : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Table](table/)(DocumentBase) | Initialisiert eine neue Instanz von **Tisch** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Ermittelt oder setzt die absolute horizontale Position der schwebenden Tabelle, die durch die Tabelleneigenschaften angegeben ist, in Punkten. Der Standardwert ist 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Ermittelt oder setzt die absolute vertikale Position der schwebenden Tabelle, die durch die Tabelleneigenschaften angegeben ist, in Punkten. Der Standardwert ist 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Gibt an, wie eine Inline-Tabelle im Dokument ausgerichtet wird. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Ermöglicht Microsoft Word und Aspose.Words, die Größe von Zellen in einer Tabelle automatisch an ihren Inhalt anzupassen. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Ruft die Option "Abstände zwischen Zellen zulassen" ab oder legt sie fest. |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Ruft ab, ob eine schwebende Tabelle anderen schwebenden Objekten im Dokument erlauben soll, ihre Grenzen zu überlappen, wenn sie angezeigt werden. Der Standardwert ist`Stimmt` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Ruft ab oder legt fest, ob es sich um eine rechts-nach-links-Tabelle handelt. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Ruft den Abstand (in Punkt) ab oder legt ihn fest, der unter dem Inhalt von Zellen hinzugefügt werden soll. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Ruft den Abstand (in Punkten) zwischen den Zellen ab oder legt ihn fest. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Ruft die Beschreibung dieser Tabelle ab oder legt sie fest. Bietet eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; } | Ermittelt den Abstand zwischen Tabellenunterkante und umgebendem Text in Punkten. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; } | Ermittelt den Abstand zwischen der linken Seite der Tabelle und dem umgebenden Text in Punkten. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; } | Ermittelt den Abstand zwischen der rechten Seite der Tabelle und dem umgebenden Text in Punkten. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; } | Ruft den Abstand zwischen der Tischplatte und dem umgebenden Text in Punkten ab. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Gibt den ersten zurück **Die Zeile** Knoten in der Tabelle. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Ruft das Basisobjekt ab, aus dem die horizontale Positionierung der schwebenden Tabelle berechnet werden soll. Standardwert istColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Gibt den letzten zurück **Die Zeile** Knoten in der Tabelle. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Ruft den Wert ab, der den linken Einzug der Tabelle darstellt, oder legt ihn fest. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Ruft den Platz (in Punkten) ab oder legt ihn fest, der links vom Inhalt der Zellen hinzugefügt werden soll. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | gibt zurück **Knotentyp.Tabelle** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Ruft die bevorzugte Tabellenbreite ab oder legt sie fest. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Ruft die relative horizontale Ausrichtung der Floating-Tabelle ab oder legt sie fest. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Ruft die relative vertikale Ausrichtung der Floating-Tabelle ab oder legt sie fest. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Ruft den Abstand (in Punkten) ab oder legt ihn fest, der rechts vom Inhalt der Zellen hinzugefügt werden soll. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Bietet typisierten Zugriff auf die Zeilen der Tabelle. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Ruft den auf diese Tabelle angewendeten Tabellenstil ab oder legt ihn fest. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Ruft den gebietsschemaunabhängigen Stilbezeichner des auf diese Tabelle angewendeten Tabellenstils ab oder legt ihn fest. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Ruft den Namen des auf diese Tabelle angewendeten Tabellenstils ab oder legt ihn fest. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Ruft Bit-Flags ab oder setzt diese, die angeben, wie ein Tabellenstil auf diese Tabelle angewendet wird. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Holt oder setzt[`TextWrapping`](./textwrapping/) für Tabelle. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Ruft den Titel dieser Tabelle ab oder legt ihn fest. Bietet eine alternative Textdarstellung der in der Tabelle enthaltenen Informationen. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Ruft den Abstand (in Punkt) ab oder legt ihn fest, der über dem Inhalt von Zellen hinzugefügt werden soll. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Ruft das Basisobjekt ab, aus dem die vertikale Positionierung der schwebenden Tabelle berechnet werden soll. Standardwert istMargin . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(AutoFitBehavior) | Ändert die Größe der Tabelle und der Zellen gemäß dem angegebenen automatischen Anpassungsverhalten. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Entfernt alle Tabellen- und Zellränder dieser Tabelle. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Entfernt alle Schattierungen auf der Tabelle. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Konvertiert Zellen, die horizontal nach Breite verbunden sind, in Zellen, die nach verbunden sind[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Wenn die Tabelle keine Zeilen hat, wird eine erstellt und angehängt **Die Zeile** . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(BorderType, LineStyle, double, Color, bool) | Setzt den angegebenen Tabellenrahmen auf die angegebene Linienart, Breite und Farbe. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(LineStyle, double, Color) | Setzt alle Tabellenrahmen auf den angegebenen Linienstil, Breite und Farbe. |
| [SetShading](../../aspose.words.tables/table/setshading/)(TextureIndex, Color, Color) | Setzt die Schattierung auf die angegebenen Werte für die gesamte Tabelle. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

**Tisch**ist ein Knoten auf Blockebene und kann ein untergeordnetes Element von abgeleiteten Klassen sein **Geschichte** oder  **InlineStory**.

**Tisch** kann eine oder mehrere enthalten **Die Zeile** Knoten.

Eine gültige Minimaltabelle muss mindestens eine haben **Die Zeile**.

### Beispiele

Zeigt, wie eine Tabelle erstellt wird.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze haben können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Das Aufrufen der "EnsureMinimum"-Methode für eine Tabelle stellt dies sicher
// Die Tabelle hat mindestens eine Zeile, eine Zelle und einen Absatz.
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

Zeigt, wie alle Tabellen im Dokument durchlaufen und der Inhalt jeder Zelle gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Wir können die "ToArray"-Methode für eine Zeilensammlung verwenden, um sie in ein Array zu klonen.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Wir können die "ToArray"-Methode für eine Zellsammlung verwenden, um sie in ein Array zu klonen.
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
// zur aktuellen Zeile/Zelle, in der sich der Cursor befindet, und zu allen neuen Zeilen/Zellen, wenn sie erstellt werden.
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

// Zuvor hinzugefügte Zeilen und Zellen sind nicht rückwirkend von Änderungen an der Formatierung des Builders betroffen.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Zeigt, wie Sie eine verschachtelte Tabelle erstellen, ohne einen Document Builder zu verwenden.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Erstellen Sie die äußere Tabelle mit drei Zeilen und vier Spalten und fügen Sie sie dann dem Dokument hinzu.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Erstellen Sie eine weitere Tabelle mit zwei Zeilen und zwei Spalten und fügen Sie sie dann in die erste Zelle der ersten Tabelle ein.
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

    // Sie können die Eigenschaften "Titel" und "Beschreibung" verwenden, um Ihrer Tabelle jeweils einen Titel und eine Beschreibung hinzuzufügen.
    // Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    // Diese Eigenschaften sind sinnvoll für ISO/IEC 29500-konforme .docx-Dokumente (siehe Klasse OoxmlCompliance).
    // Wenn wir das Dokument in Pre-ISO/IEC 29500-Formaten speichern, ignoriert Microsoft Word diese Eigenschaften.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode/)
* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
