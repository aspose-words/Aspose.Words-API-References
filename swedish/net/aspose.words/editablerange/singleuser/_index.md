---
title: EditableRange.SingleUser
linktitle: SingleUser
articleTitle: SingleUser
second_title: Aspose.Words för .NET
description: Upptäck egenskapen EditableRange SingleUser för att effektivt hantera redigerbara intervall, vilket säkerställer sömlöst samarbete och användarspecifik åtkomstkontroll.
type: docs
weight: 50
url: /sv/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Returnerar eller ställer in den enskilda användaren för redigerbart område.

```csharp
public string SingleUser { get; set; }
```

## Anmärkningar

Denna redigerare kan lagras i en av följande former:

DOMÄN\Användarnamn - för användare vars åtkomst ska autentiseras med den aktuella användarens domänuppgifter.

användare@domän.com – för användare vars åtkomst ska autentiseras med användarens e-postadress som inloggningsuppgifter.

användare - för användare vars åtkomst ska autentiseras med den aktuella användarens maskinuppgifter.

En enda användare och redigeringsgrupp kan inte ställas in samtidigt för det specifika redigerbara området. om den ena är inställd kommer den andra att vara tom.

## Exempel

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

* class [EditableRange](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
