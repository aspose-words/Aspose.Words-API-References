---
title: EditableRange.SingleUser
linktitle: SingleUser
articleTitle: SingleUser
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „EditableRange SingleUser“, um bearbeitbare Bereiche effizient zu verwalten und so eine nahtlose Zusammenarbeit und benutzerspezifische Zugriffskontrolle sicherzustellen.
type: docs
weight: 50
url: /de/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Gibt den einzelnen Benutzer für den bearbeitbaren Bereich zurück oder legt ihn fest.

```csharp
public string SingleUser { get; set; }
```

## Bemerkungen

Dieser Editor kann in einer der folgenden Formen gespeichert werden:

DOMÄNE\Benutzername – für Benutzer, deren Zugriff mit den Domänenanmeldeinformationen des aktuellen Benutzers authentifiziert werden soll.

user@domain.com – für Benutzer, deren Zugriff mithilfe der E-Mail-Adresse des Benutzers als Anmeldeinformationen authentifiziert werden soll.

Benutzer – für Benutzer, deren Zugriff mit den Computeranmeldeinformationen des aktuellen Benutzers authentifiziert werden soll.

Für den spezifischen bearbeitbaren Bereich können nicht gleichzeitig ein einzelner Benutzer und eine Editorgruppe festgelegt werden. Wenn einer festgelegt ist, bleibt der andere gelöscht.

## Beispiele

Zeigt, wie die Bearbeitungsrechte bearbeitbarer Bereiche auf eine bestimmte Gruppe/einen bestimmten Benutzer beschränkt werden.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Wenn wir Dokumente mit einem Schreibschutz versehen, können wir mithilfe bearbeitbarer Bereiche bestimmte Bereiche auswählen, die Benutzer bearbeiten dürfen.
    // Es gibt zwei sich gegenseitig ausschließende Möglichkeiten, die Liste der zulässigen Editoren einzugrenzen.
    // 1 - Geben Sie einen Benutzer an:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - Geben Sie eine Gruppe an, der zulässige Benutzer zugeordnet sind:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Details und Inhalte jedes bearbeitbaren Bereichs im Dokument drucken.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Sammelt Eigenschaften und Inhalte der besuchten bearbeitbaren Bereiche in einer Zeichenfolge.
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
    /// Wird aufgerufen, wenn im Dokument ein EditableRangeStart-Knoten gefunden wird.
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
    /// Wird aufgerufen, wenn im Dokument ein EditableRangeEnd-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein Run-Knoten gefunden wird. Dieser Besucher zeichnet nur Läufe auf, die innerhalb bearbeitbarer Bereiche liegen.
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

### Siehe auch

* class [EditableRange](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
