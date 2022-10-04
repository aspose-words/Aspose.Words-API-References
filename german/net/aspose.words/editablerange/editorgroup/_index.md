---
title: EditorGroup
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt einen Alias oder eine Bearbeitungsgruppe zurück oder legt ihn fest der verwendet werden soll um zu bestimmen ob der aktuelle Benutzer diesen bearbeitbaren Bereich bearbeiten darf.
type: docs
weight: 30
url: /de/net/aspose.words/editablerange/editorgroup/
---
## EditableRange.EditorGroup property

Gibt einen Alias (oder eine Bearbeitungsgruppe) zurück oder legt ihn fest, der verwendet werden soll, um zu bestimmen, ob der aktuelle Benutzer diesen bearbeitbaren Bereich bearbeiten darf.

```csharp
public EditorType EditorGroup { get; set; }
```

### Bemerkungen

Einzelbenutzer und Editorgruppe können nicht gleichzeitig für den spezifischen bearbeitbaren Bereich eingestellt werden, wenn der eine eingestellt ist, wird der andere gelöscht.

### Beispiele

Zeigt, wie verschachtelte bearbeitbare Bereiche erstellt werden.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Zwei verschachtelte bearbeitbare Bereiche erstellen.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Derzeit befindet sich der Einfügecursor des Document Builder in mehr als einem fortlaufend bearbeitbaren Bereich.
// Wenn wir in dieser Situation einen bearbeitbaren Bereich beenden möchten,
// Wir müssen angeben, welchen der Bereiche wir beenden möchten, indem wir seinen EditableRangeStart-Knoten übergeben.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Wenn ein Textbereich zwei überlappende bearbeitbare Bereiche mit angegebenen Gruppen hat,
// Die kombinierte Gruppe von Benutzern, die von beiden Gruppen ausgeschlossen wurden, wird daran gehindert, sie zu bearbeiten.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

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

* enum [EditorType](../../editortype/)
* class [EditableRange](../)
* namensraum [Aspose.Words](../../editablerange/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
