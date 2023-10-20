---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: Aspose.Words für .NET
description: Aspose.Words.EditorType opsomming. Gibt den Satz möglicher Aliase oder Bearbeitungsgruppen an die als Aliase verwendet werden können um zu bestimmen ob der aktuelle Benutzer einen einzelnen Bereich bearbeiten darf der durch einen bearbeitbaren Bereich innerhalb eines Dokuments definiert ist in C#.
type: docs
weight: 1450
url: /de/net/aspose.words/editortype/
---
## EditorType enumeration

Gibt den Satz möglicher Aliase (oder Bearbeitungsgruppen) an, die als Aliase verwendet werden können, um zu bestimmen, ob der aktuelle Benutzer einen einzelnen Bereich bearbeiten darf, der durch einen bearbeitbaren Bereich innerhalb eines Dokuments definiert ist.

```csharp
public enum EditorType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Unspecified | `0` | Bedeutet, dass der Editortyp nicht angegeben ist. |
| Administrators | `1` | Gibt an, dass Benutzer, die der Gruppe „Administratoren“ zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentschutz aktiviert ist. |
| Contributors | `2` | Gibt an, dass Benutzer, die der Gruppe „Mitwirkende“ zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentschutz aktiviert ist. |
| Current | `3` | Gibt an, dass Benutzer, die der aktuellen Gruppe zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentschutz aktiviert ist. |
| Editors | `4` | Gibt an, dass Benutzer, die der Gruppe „Editoren“ zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentschutz aktiviert ist. |
| Everyone | `5` | Gibt an, dass alle Benutzer, die das Dokument öffnen, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentschutz aktiviert ist. |
| None | `6` | Gibt an, dass keiner der Benutzer, die das Dokument öffnen, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten darf, wenn der Dokumentschutz aktiviert ist. |
| Owners | `7` | Gibt an, dass Benutzer, die der Gruppe „Besitzer“ zugeordnet sind, bearbeitbare Bereiche mit diesem Bearbeitungstyp bearbeiten dürfen, wenn der Dokumentschutz aktiviert ist. |
| Default | `0` | Das Gleiche wieUnspecified . |

## Beispiele

Zeigt, wie man die Bearbeitungsrechte bearbeitbarer Bereiche auf eine bestimmte Gruppe/einen bestimmten Benutzer beschränkt.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Wenn wir Dokumente mit einem Schreibschutz versehen, ermöglichen uns bearbeitbare Bereiche die Auswahl bestimmter Bereiche, die Benutzer bearbeiten dürfen.
    // Es gibt zwei sich gegenseitig ausschließende Möglichkeiten, die Liste der zulässigen Editoren einzugrenzen.
    // 1 – Geben Sie einen Benutzer an:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 – Geben Sie eine Gruppe an, der zulässige Benutzer zugeordnet sind:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Details und Inhalte aller bearbeitbaren Bereiche im Dokument drucken.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Sammelt Eigenschaften und Inhalte der besuchten bearbeitbaren Bereiche in einem String.
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
