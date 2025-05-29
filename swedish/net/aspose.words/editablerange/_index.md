---
title: EditableRange Class
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.EditableRange, din lösning för att enkelt hantera redigerbara textområden. Förbättra dokumentredigering med lätthet!
type: docs
weight: 1830
url: /sv/net/aspose.words/editablerange/
---
## EditableRange class

Representerar ett enda redigerbart område.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public class EditableRange
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | Hämtar noden som representerar slutet av det redigerbara området. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | Hämtar noden som representerar början av det redigerbara området. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | Returnerar eller anger ett alias (eller en redigeringsgrupp) som ska användas för att avgöra om den aktuella användaren ska ha tillstånd att redigera detta redigerbara område. |
| [Id](../../aspose.words/editablerange/id/) { get; } | Hämtar den redigerbara intervallidentifieraren. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | Returnerar eller ställer in den enskilda användaren för redigerbart område. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | Tar bort det redigerbara området från dokumentet. Tar inte bort innehåll inom det redigerbara området. |

## Anmärkningar

`EditableRange` är ett "fasadobjekt" som inkapslar två noder[`EditableRangeStart`](./editablerangestart/) och[`EditableRangeEnd`](./editablerangeend/) i ett dokumentträd och tillåter att arbeta med ett redigerbart område som ett enda objekt.

## Exempel

Visar hur man arbetar med ett redigerbart område.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Redigerbara områden låter oss lämna delar av skyddade dokument öppna för redigering.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Ett välformat redigerbart område har en startnod och en slutnod.
// Dessa noder har matchande ID:n och omfattar redigerbara noder.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Olika delar av det redigerbara området länkar till varandra.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Vi kan komma åt nodtyperna för varje del så här. Det redigerbara området i sig är inte en nod,
// men en enhet som består av en början, ett slut och deras inneslutna innehåll.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Ta bort ett redigerbart område. Alla noder som fanns inom området kommer att förbli intakta.
editableRange.Remove();
```

Visar hur man begränsar redigeringsrättigheterna för redigerbara områden till en specifik grupp/användare.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // När vi skrivskyddar dokument tillåter redigerbara områden oss att välja specifika områden som användare kan redigera.
    // Det finns två ömsesidigt uteslutande sätt att begränsa listan över tillåtna redigerare.
    // 1 - Ange en användare:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Ange en grupp som tillåtna användare är associerade med:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Skriv ut detaljer och innehåll för alla redigerbara områden i dokumentet.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Samlar in egenskaper och innehåll från besökta redigerbara områden i en sträng.
/// </summary>
public class EditableRangePrinter : DocumentVisitor
{
    public EditableRangePrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string ToText()
    {
        return mBuilder.ToString();
    }

    public void Reset()
    {
        mBuilder.Clear();
        mInsideEditableRange = false;
    }

    /// <summary>
    /// Anropas när en EditableRangeStart-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        mBuilder.AppendLine(" -- Editable range found! -- ");
        mBuilder.AppendLine("\tID:\t\t" + editableRangeStart.Id);
        if (editableRangeStart.EditableRange.SingleUser == string.Empty)
            mBuilder.AppendLine("\tGroup:\t" + editableRangeStart.EditableRange.EditorGroup);
        else
            mBuilder.AppendLine("\tUser:\t" + editableRangeStart.EditableRange.SingleUser);
        mBuilder.AppendLine("\tContents:");

        mInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en EditableRangeEnd-nod påträffas i dokumentet.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när en Run-nod påträffas i dokumentet. Den här besökaren registrerar endast körningar som ligger inom redigerbara intervall.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mInsideEditableRange) mBuilder.AppendLine("\t\"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    private bool mInsideEditableRange;
    private readonly StringBuilder mBuilder;
}
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
