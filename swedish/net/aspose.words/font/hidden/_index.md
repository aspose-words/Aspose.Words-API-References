---
title: Font.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Dolt teckensnitt. Identifiera enkelt om din text är formaterad som dold. Förbättra ditt dokuments tydlighet och presentation idag!
type: docs
weight: 140
url: /sv/net/aspose.words/font/hidden/
---
## Font.Hidden property

Sant om teckensnittet är formaterat som dold text.

```csharp
public bool Hidden { get; set; }
```

## Exempel

Visar hur man skapar en serie dold text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Med flaggan Hidden satt till true kommer all text som vi skapar med detta Font-objekt att vara osynlig i dokumentet.
// Vi kommer inte att se eller markera dold text om vi inte aktiverar alternativet "Dold text"
// hittades i Microsoft Word via "Arkiv" -> "Alternativ" -> "Visa". Texten kommer fortfarande att finnas där,
// och vi kommer att kunna komma åt den här texten programmatiskt.
// Det rekommenderas inte att använda den här metoden för att dölja känslig information.
builder.Font.Hidden = true;
builder.Font.Size = 36;

builder.Writeln("This text will not be visible in the document.");

doc.Save(ArtifactsDir + "Font.Hidden.docx");
```

Visar hur man använder en DocumentVisitor-implementering för att ta bort allt dolt innehåll från ett dokument.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Nedan finns tre typer av fält som kan acceptera en dokumentbesökare,
    // vilket gör att den kan besöka den accepterande noden och sedan korsa dess undernoder på ett djup-först-sätt.
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
    /// Anropas när en Run-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en styckenod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när ett FormField påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en gruppform påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en form påträffas i dokumentet.
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
    /// Anropas när ett SpecialCharacter påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när besöket till en tabellnod i dokumentet avslutas.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Innehållet i tabellceller kan ha flaggan för dolt innehåll, men tabellerna själva kan inte det.
        // Om den här tabellen bara hade dolt innehåll, skulle besökaren ha tagit bort allt,
        // och det skulle inte finnas några undernoder kvar.
        // Således kan vi också behandla själva tabellen som dolt innehåll och ta bort det.
        // Tabeller som är tomma men inte har dolt innehåll kommer att ha celler med tomma stycken inuti,
        // som den här besökaren inte kommer att ta bort.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när besöket av en cellnod avslutas i dokumentet.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när besöket på en radnod i dokumentet avslutas.
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

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
