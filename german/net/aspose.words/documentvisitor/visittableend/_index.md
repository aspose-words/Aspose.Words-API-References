---
title: DocumentVisitor.VisitTableEnd
linktitle: VisitTableEnd
articleTitle: VisitTableEnd
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentVisitor-Methode VisitTableEnd, die das Ende der Tabellenaufzählung effizient signalisiert und so Ihre Codiererfahrung verbessert.
type: docs
weight: 490
url: /de/net/aspose.words/documentvisitor/visittableend/
---
## DocumentVisitor.VisitTableEnd method

Wird aufgerufen, wenn die Aufzählung einer Tabelle beendet ist.

```csharp
public virtual VisitorAction VisitTableEnd(Table table)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | Table | Das Objekt, das besucht wird. |

### Rückgabewert

A[`VisitorAction`](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.

## Beispiele

Zeigt, wie die Knotenstruktur jeder Tabelle in einem Dokument gedruckt wird.

```csharp
public void TableToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    TableStructurePrinter visitor = new TableStructurePrinter();

    // Wenn wir einen zusammengesetzten Knoten dazu bringen, einen Dokumentbesucher zu akzeptieren, besucht der Besucher den akzeptierenden Knoten.
    // und durchläuft dann alle untergeordneten Knoten in einer Tiefensuche.
    // Der Besucher kann jeden besuchten Knoten lesen und ändern.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Durchläuft den nicht-binären Baum der untergeordneten Knoten eines Knotens.
/// Erstellt eine Karte in Form einer Zeichenfolge aller gefundenen Tabellenknoten und ihrer untergeordneten Elemente.
/// </summary>
public class TableStructurePrinter : DocumentVisitor
{
    public TableStructurePrinter()
    {
        mVisitedTables = new StringBuilder();
        mVisitorIsInsideTable = false;
    }

    public string GetText()
    {
        return mVisitedTables.ToString();
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// Läufe, die nicht in Tabellen liegen, werden nicht aufgezeichnet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideTable) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine Tabelle gefunden wird.
    /// </summary>
    public override VisitorAction VisitTableStart(Table table)
    {
        int rows = 0;
        int columns = 0;

        if (table.Rows.Count > 0)
        {
            rows = table.Rows.Count;
            columns = table.FirstRow.Count;
        }

        IndentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
        mDocTraversalDepth++;
        mVisitorIsInsideTable = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Tabellenknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Table end]");
        mVisitorIsInsideTable = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Zeilenknoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRowStart(Row row)
    {
        string rowContents = row.GetText().TrimEnd(new []{ '\u0007', ' ' }).Replace("\u0007", ", ");
        int rowWidth = row.IndexOf(row.LastCell) + 1;
        int rowIndex = row.ParentTable.IndexOf(row);
        string rowStatusInTable = row.IsFirstRow && row.IsLastRow ? "only" : row.IsFirstRow ? "first" : row.IsLastRow ? "last" : "";
        if (rowStatusInTable != "")
        {
            rowStatusInTable = $", the {rowStatusInTable} row in this table,";
        }

        IndentAndAppendLine($"[Row start] Row #{++rowIndex}{rowStatusInTable} width {rowWidth}, \"{rowContents}\"");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Zeilenknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Row end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Zellknoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitCellStart(Cell cell)
    {
        Row row = cell.ParentRow;
        Table table = row.ParentTable;
        string cellStatusInRow = cell.IsFirstCell && cell.IsLastCell ? "only" : cell.IsFirstCell ? "first" : cell.IsLastCell ? "last" : "";
        if (cellStatusInRow != "")
        {
            cellStatusInRow = $", the {cellStatusInRow} cell in this row";
        }

        IndentAndAppendLine($"[Cell start] Row {table.IndexOf(row) + 1}, Col {row.IndexOf(cell) + 1}{cellStatusInRow}");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, nachdem alle untergeordneten Knoten eines Zellknotens besucht wurden.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Cell end]");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Fügen Sie dem StringBuilder eine Zeile hinzu und rücken Sie diese ein, je nachdem, wie tief der Besucher ist
    /// in den Baum der untergeordneten Knoten der aktuellen Tabelle.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mVisitedTables.Append("|  ");
        }

        mVisitedTables.AppendLine(text);
    }

    private bool mVisitorIsInsideTable;
    private int mDocTraversalDepth;
    private readonly StringBuilder mVisitedTables;
}
```

Zeigt, wie Sie mithilfe einer DocumentVisitor-Implementierung alle ausgeblendeten Inhalte aus einem Dokument entfernen.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Unten sind drei Arten von Feldern aufgeführt, die einen Dokumentbesucher akzeptieren können.
    // Dadurch kann es den akzeptierenden Knoten besuchen und dann seine untergeordneten Knoten in einer Tiefensuche durchlaufen.
    // 1 - Absatzknoten:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tabellenknoten:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Dokumentknoten:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// Entfernt alle besuchten Knoten, die als „versteckter Inhalt“ markiert sind.
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldStart-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldEnd-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldSeparator-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Absatzknoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FormField gefunden wird.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine GroupShape gefunden wird.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine Form gefunden wird.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Kommentar gefunden wird.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument eine Fußnote gefunden wird.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Sonderzeichen gefunden wird.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Tabellenknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Der Inhalt in Tabellenzellen kann das Flag für ausgeblendeten Inhalt haben, die Tabellen selbst jedoch nicht.
        // Wenn diese Tabelle nur versteckte Inhalte hätte, hätte dieser Besucher alles entfernt.
        // und es wären keine untergeordneten Knoten übrig.
        // Daher können wir auch die Tabelle selbst als versteckten Inhalt behandeln und entfernen.
        // Tabellen, die leer sind, aber keinen versteckten Inhalt haben, enthalten Zellen mit leeren Absätzen.
        // die dieser Besucher nicht entfernen wird.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Zellknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Zeilenknotens im Dokument beendet ist.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Siehe auch

* enum [VisitorAction](../../visitoraction/)
* class [Table](../../../aspose.words.tables/table/)
* class [DocumentVisitor](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
