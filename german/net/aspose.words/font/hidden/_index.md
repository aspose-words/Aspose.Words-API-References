---
title: Hidden
second_title: Aspose.Words für .NET-API-Referenz
description: Wahr wenn die Schriftart als verborgener Text formatiert ist.
type: docs
weight: 140
url: /de/net/aspose.words/font/hidden/
---
## Font.Hidden property

Wahr, wenn die Schriftart als verborgener Text formatiert ist.

```csharp
public bool Hidden { get; set; }
```

### Beispiele

Zeigt, wie eine Reihe von verborgenem Text erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn das Hidden-Flag auf true gesetzt ist, ist jeder Text, den wir mit diesem Font-Objekt erstellen, im Dokument unsichtbar.
// Wir werden verborgenen Text weder sehen noch hervorheben, es sei denn, wir aktivieren die Option „Versteckter Text“.
// gefunden in Microsoft Word über "Datei" -> "Optionen" -> "Anzeige". Der Text wird immer noch da sein,
// und wir können programmgesteuert auf diesen Text zugreifen.
// Es wird nicht empfohlen, diese Methode zu verwenden, um vertrauliche Informationen zu verbergen.
builder.Font.Hidden = true;
builder.Font.Size = 36;

builder.Writeln("This text will not be visible in the document.");

doc.Save(ArtifactsDir + "Font.Hidden.docx");
```

Zeigt, wie eine DocumentVisitor-Implementierung verwendet wird, um alle ausgeblendeten Inhalte aus einem Dokument zu entfernen.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Unten sind drei Arten von Feldern, die einen Dokumentbesucher akzeptieren können,
    // was es ihm ermöglicht, den akzeptierenden Knoten zu besuchen und dann seine untergeordneten Knoten in einer Tiefe-zuerst-Weise zu durchlaufen.
    // 1 - Absatzknoten:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tabellenknoten:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Dokumentenknoten:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// Entfernt alle besuchten Knoten, die als "versteckter Inhalt" markiert sind.
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
    /// Wird aufgerufen, wenn im Dokument ein Paragraph-Knoten gefunden wird.
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
    /// Wird aufgerufen, wenn im Dokument ein GroupShape gefunden wird.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Shape gefunden wird.
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
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Tabellenknotens im Dokument beendet wird.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Der Inhalt innerhalb von Tabellenzellen kann das Hidden-Content-Flag haben, die Tabellen selbst jedoch nicht.
        // Wenn diese Tabelle nur versteckte Inhalte hätte, hätte dieser Besucher alles davon entfernt,
        // und es gäbe keine untergeordneten Knoten mehr.
        // Somit können wir auch die Tabelle selbst als versteckten Inhalt behandeln und entfernen.
        // Tabellen, die leer sind, aber keinen versteckten Inhalt haben, haben Zellen mit leeren Absätzen darin,
        // die dieser Besucher nicht entfernen wird.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Cell-Knotens im Dokument beendet wird.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines Zeilenknotens im Dokument beendet wird.
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

* class [Font](../../font)
* namensraum [Aspose.Words](../../font)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
