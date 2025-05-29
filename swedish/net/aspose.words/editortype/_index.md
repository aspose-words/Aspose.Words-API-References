---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.EditorType, som definierar redigeringsgrupper för att kontrollera användarbehörigheter för redigering av dokumentintervall. Förbättra din dokumenthantering idag!
type: docs
weight: 1860
url: /sv/net/aspose.words/editortype/
---
## EditorType enumeration

Anger uppsättningen möjliga alias (eller redigeringsgrupper) som kan användas som alias för att avgöra om den aktuella användaren ska tillåtas redigera ett enskilt område som definieras av ett redigerbart område inom ett dokument.

```csharp
public enum EditorType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Unspecified | `0` | Betyder att editortypen inte är specificerad. |
| Administrators | `1` | Anger att användare som är associerade med gruppen Administratörer ska ha rätt att redigera redigerbara områden med hjälp av denna redigeringstyp när dokumentskydd är aktiverat. |
| Contributors | `2` | Anger att användare som är associerade med gruppen Bidragsgivare ska ha rätt att redigera redigerbara områden med hjälp av denna redigeringstyp när dokumentskydd är aktiverat. |
| Current | `3` | Anger att användare som är associerade med den aktuella gruppen ska tillåtas redigera redigerbara områden med denna redigeringstyp när dokumentskydd är aktiverat. |
| Editors | `4` | Anger att användare som är associerade med gruppen Redigerare ska ha rätt att redigera redigerbara områden med denna redigeringstyp när dokumentskydd är aktiverat. |
| Everyone | `5` | Anger att alla användare som öppnar dokumentet ska ha rätt att redigera redigerbara områden med hjälp av den här typen editing när dokumentskydd är aktiverat. |
| None | `6` | Anger att ingen av användarna som öppnar dokumentet ska tillåtas redigera redigerbara områden med denna redigeringstyp när dokumentskydd är aktiverat. |
| Owners | `7` | Anger att användare som är associerade med gruppen Ägare ska ha rätt att redigera redigerbara områden med denna redigeringstyp när dokumentskydd är aktiverat. |
| Default | `0` | Samma somUnspecified . |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
