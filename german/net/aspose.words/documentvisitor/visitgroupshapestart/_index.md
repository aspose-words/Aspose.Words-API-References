---
title: DocumentVisitor.VisitGroupShapeStart
linktitle: VisitGroupShapeStart
articleTitle: VisitGroupShapeStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentVisitor VisitGroupShapeStart-Methode, die für eine effiziente Gruppenform-Aufzählung in Ihren Anwendungen unerlässlich ist. Optimieren Sie noch heute Ihren Codier-Workflow!
type: docs
weight: 270
url: /de/net/aspose.words/documentvisitor/visitgroupshapestart/
---
## DocumentVisitor.VisitGroupShapeStart method

Wird aufgerufen, wenn die Aufzählung einer Gruppenform begonnen hat.

```csharp
public virtual VisitorAction VisitGroupShapeStart(GroupShape groupShape)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| groupShape | GroupShape | Das Objekt, das besucht wird. |

### Rückgabewert

A[`VisitorAction`](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.

## Beispiele

Zeigt, wie Sie eine Gruppe von Formen erstellen und deren Inhalt mithilfe eines Dokumentbetrachters drucken.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // Eine abgerundete obere Ecke, eine abgeschnittene Ecke, eine abgerundete obere Ecke, abgerundete diagonale Ecke
    // Bitte verwenden Sie DocumentBuilder.InsertShape-Methoden.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200,
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100,
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Gibt den Inhalt einer besuchten Formgruppe auf der Konsole aus.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
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
* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [DocumentVisitor](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
