---
title: DocumentVisitor.VisitGroupShapeStart
second_title: Aspose.Words för .NET API Referens
description: DocumentVisitor metod. Anropas när uppräkningen av en gruppform har börjat.
type: docs
weight: 270
url: /sv/net/aspose.words/documentvisitor/visitgroupshapestart/
---
## DocumentVisitor.VisitGroupShapeStart method

Anropas när uppräkningen av en gruppform har börjat.

```csharp
public virtual VisitorAction VisitGroupShapeStart(GroupShape groupShape)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| groupShape | GroupShape | Objektet som besöks. |

### Returvärde

A[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

### Exempel

Visar hur man skapar en grupp av former och skriver ut dess innehåll med hjälp av en dokumentbesökare.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Om du behöver skapa "NonPrimitive" former, som SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // använd DocumentBuilder.InsertShape metoder.
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
/// Skriver ut innehållet i en besökt formgrupp till konsolen.
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

Visar hur man använder en DocumentVisitor-implementering för att ta bort allt dolt innehåll från ett dokument.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Nedan finns tre typer av fält som kan acceptera en dokumentbesökare,
    // som gör det möjligt för den att besöka den accepterande noden och sedan korsa dess underordnade noder på ett djupt-först sätt.
    // 1 - Styckenod:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tabellnod:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Dokumentnod:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

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
* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../documentvisitor/)
* hopsättning [Aspose.Words](../../../)


