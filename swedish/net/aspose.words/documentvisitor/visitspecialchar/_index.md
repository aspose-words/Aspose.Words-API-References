---
title: DocumentVisitor.VisitSpecialChar
second_title: Aspose.Words för .NET API Referens
description: DocumentVisitor metod. Ringde när enSpecialChar nod påträffas i dokumentet.
type: docs
weight: 430
url: /sv/net/aspose.words/documentvisitor/visitspecialchar/
---
## DocumentVisitor.VisitSpecialChar method

Ringde när en[`SpecialChar`](../../specialchar/) nod påträffas i dokumentet.

```csharp
public virtual VisitorAction VisitSpecialChar(SpecialChar specialChar)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| specialChar | SpecialChar | Objektet som besöks. |

### Returvärde

A[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

### Anmärkningar

Denna metod kallas inte för generiska kontrolltecken (se[`ControlChar`](../../controlchar/) ) som kan finnas i dokumentet.

### Exempel

Visar hur man använder en DocumentVisitor-implementering för att ta bort allt dolt innehåll från ett dokument.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Nedan finns tre typer av fält som kan acceptera en dokumentbesökare,
    // som gör det möjligt för den att besöka den accepterande noden och sedan korsa dess underordnade noder på ett djupt-först sätt.
    // 1 - Styckenod:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tabellnod:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Dokumentnod:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// Tar bort alla besökta noder markerade som "dolt innehåll".
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Anropas när en FieldStart-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldEnd-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en FieldSeparator-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en körnod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Paragraph-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när ett formulärfält påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en GroupShape påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Shape påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en kommentar påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en fotnot påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en specialtecken påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas vid besök av en Tabellnod avslutas i dokumentet.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Innehållet i tabellceller kan ha den dolda innehållsflaggan, men tabellerna själva kan inte.
        // Om denna tabell inte hade något annat än dolt innehåll, skulle den här besökaren ha tagit bort allt,
        // och det skulle inte finnas några barnnoder kvar.
        // Således kan vi också behandla själva tabellen som dolt innehåll och ta bort det.
        // Tabeller som är tomma men inte har dolt innehåll kommer att ha celler med tomma stycken inuti,
        // som den här besökaren inte kommer att ta bort.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när besök av en cellnod avslutas i dokumentet.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när besök av en radnod avslutas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Se även

* enum [VisitorAction](../../visitoraction/)
* class [SpecialChar](../../specialchar/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../documentvisitor/)
* hopsättning [Aspose.Words](../../../)


