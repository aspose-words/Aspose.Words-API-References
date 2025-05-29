---
title: Cell Class
linktitle: Cell
articleTitle: Cell
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Tables.Cell – Ihre Lösung für effizientes Tabellenzellenmanagement in der Dokumentenverarbeitung. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 7090
url: /de/net/aspose.words.tables/cell/
---
## Cell class

Stellt eine Tabellenzelle dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Tabellen](https://docs.aspose.com/words/net/working-with-tables/) Dokumentationsartikel.

```csharp
public class Cell : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Cell](cell/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initialisiert eine neue Instanz des`Cell` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat/) { get; } | Bietet Zugriff auf die Formatierungseigenschaften der Zelle. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph/) { get; } | Ruft den ersten Absatz unter den unmittelbar untergeordneten Elementen ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell/) { get; } | Wahr, wenn dies die erste Zelle in einer Zeile ist, andernfalls falsch. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell/) { get; } | Wahr, wenn dies die letzte Zelle in einer Zeile ist, andernfalls falsch. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph/) { get; } | Ruft den letzten Absatz unter den unmittelbar untergeordneten Elementen ab. |
| [NextCell](../../aspose.words.tables/cell/nextcell/) { get; } | Ruft den nächsten`Cell` Knoten. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.tables/cell/nodetype/) { get; } | RückgabenCell . |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Zelle sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentRow](../../aspose.words.tables/cell/parentrow/) { get; } | Gibt die übergeordnete Zeile der Zelle zurück. |
| [PreviousCell](../../aspose.words.tables/cell/previouscell/) { get; } | Ruft die vorherige`Cell` Knoten. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Tables](../../aspose.words.tables/cell/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbare untergeordnete Elemente der Zelle sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words.tables/cell/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Zellenendes. |
| override [AcceptStart](../../aspose.words.tables/cell/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Zellenanfangs. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum/)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../../aspose.words/node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

`Cell` kann nur ein Kind eines[`Row`](../row/).

`Cell` kann Knoten auf Blockebene enthalten[`Paragraph`](../../aspose.words/paragraph/) Und[`Table`](../table/).

Eine minimal gültige Zelle muss mindestens eine[`Paragraph`](../../aspose.words/paragraph/).

## Beispiele

Zeigt, wie eine Tabelle erstellt wird.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tabellen enthalten Zeilen, die Zellen enthalten, die Absätze enthalten können
// mit typischen Elementen wie Läufen, Formen und sogar anderen Tabellen.
// Der Aufruf der Methode "EnsureMinimum" für eine Tabelle stellt sicher, dass
// Die Tabelle hat mindestens eine Zeile, Zelle und einen Absatz.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Fügen Sie der ersten Zelle in der ersten Zeile der Tabelle Text hinzu.
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

    // Wir können die Methode „ToArray“ auf eine Zeilensammlung anwenden, um sie in ein Array zu klonen.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Wir können die Methode „ToArray“ auf eine Zellensammlung anwenden, um sie in ein Array zu klonen.
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

Zeigt, wie eine verschachtelte Tabelle ohne Verwendung eines Dokumentgenerators erstellt wird.

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

    // Mit den Eigenschaften „Titel“ und „Beschreibung“ können Sie Ihrer Tabelle jeweils einen Titel und eine Beschreibung hinzufügen.
    // Die Tabelle muss mindestens eine Zeile haben, bevor wir diese Eigenschaften verwenden können.
    // Diese Eigenschaften sind für ISO/IEC 29500-konforme .docx-Dokumente von Bedeutung (siehe Klasse OoxmlCompliance).
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
