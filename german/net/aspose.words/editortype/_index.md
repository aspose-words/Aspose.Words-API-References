---
title: EditorType
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt den Satz möglicher Aliase oder Bearbeitungsgruppen an die als Aliase verwendet werden können um festzulegen ob der aktuelle Benutzer berechtigt sein soll einen einzelnen Bereich zu bearbeiten der durch einen bearbeitbaren Bereich innerhalb eines Dokuments definiert ist.
type: docs
weight: 1300
url: /de/net/aspose.words/editortype/
---
## EditorType enumeration

Gibt den Satz möglicher Aliase (oder Bearbeitungsgruppen) an, die als Aliase verwendet werden können, um festzulegen, ob der aktuelle Benutzer berechtigt sein soll, einen einzelnen Bereich zu bearbeiten, der durch einen bearbeitbaren Bereich innerhalb eines Dokuments definiert ist.

```csharp
public enum EditorType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unspecified | `0` | bedeutet, dass der Editortyp nicht angegeben ist. |
| Administrators | `1` | Gibt an, dass Benutzer, die der Gruppe Administratoren zugeordnet sind, berechtigt sein sollen, bearbeitbare Bereiche mit diesem Bearbeitungstyp zu bearbeiten, wenn der Dokumentenschutz aktiviert ist. |
| Contributors | `2` | Gibt an, dass Benutzer, die der Gruppe „Mitwirkende“ zugeordnet sind, berechtigt sein sollen, bearbeitbare Bereiche mit diesem Bearbeitungstyp zu bearbeiten, wenn der Dokumentenschutz aktiviert ist. |
| Current | `3` | Gibt an, dass Benutzer, die der aktuellen Gruppe zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Editors | `4` | Gibt an, dass Benutzer, die der Gruppe „Editoren“ zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Everyone | `5` | Gibt an, dass alle Benutzer, die das Dokument öffnen, berechtigt sein sollen, bearbeitbare Bereiche mit diesem Bearbeitungstyp zu bearbeiten, wenn der Dokumentenschutz aktiviert ist. |
| None | `6` | Gibt an, dass keiner der Benutzer, die das Dokument öffnen, berechtigt sein soll, bearbeitbare Bereiche mit dieser Bearbeitungsart zu bearbeiten, wenn der Dokumentenschutz aktiviert ist. |
| Owners | `7` | Gibt an, dass Benutzer, die der Eigentümergruppe zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentenschutz aktiviert ist. |
| Default | `0` | Gleich wieUnspecified . |

### Beispiele

Zeigt, wie die Bearbeitungsrechte von bearbeitbaren Bereichen auf eine bestimmte Gruppe/Benutzer beschränkt werden.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Wenn wir Dokumente mit Schreibschutz versehen, ermöglichen uns bearbeitbare Bereiche, bestimmte Bereiche auszuwählen, die Benutzer bearbeiten können.
    // Es gibt zwei sich gegenseitig ausschließende Möglichkeiten, die Liste der erlaubten Editoren einzugrenzen.
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

    // Details und Inhalt jedes bearbeitbaren Bereichs im Dokument drucken.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Sammelt Eigenschaften und Inhalte besuchter bearbeitbarer Bereiche in einem String.
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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
