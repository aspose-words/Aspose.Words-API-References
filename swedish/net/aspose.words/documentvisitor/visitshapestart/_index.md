---
title: DocumentVisitor.VisitShapeStart
linktitle: VisitShapeStart
articleTitle: VisitShapeStart
second_title: Aspose.Words för .NET
description: Utforska DocumentVisitor VisitShapeStart-metoden för att förbättra formuppräkningen i dina applikationer. Öka effektiviteten och effektivisera din kodningsprocess!
type: docs
weight: 400
url: /sv/net/aspose.words/documentvisitor/visitshapestart/
---
## DocumentVisitor.VisitShapeStart method

Anropas när uppräkningen av en form har påbörjats.

```csharp
public virtual VisitorAction VisitShapeStart(Shape shape)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| shape | Shape | Objektet som besöks. |

### Returvärde

En[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

## Exempel

Visar hur man skapar en grupp med former och skriver ut dess innehåll med hjälp av en dokumentbesökare.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Om du behöver skapa "Icke-primitiva" former, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // ÖvreHörnEttRundatEttBeskärt, EnkeltHörnRundat, ÖvreHörnRundade, DiagonalaHörnRundade
    // använd DocumentBuilder.InsertShape-metoderna.
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

* enum [VisitorAction](../../visitoraction/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
