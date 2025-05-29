---
title: EditableRange Class
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.EditableRange, Ihre Lösung für die mühelose Verwaltung editierbarer Textbereiche. Optimieren Sie die Dokumentbearbeitung mit Leichtigkeit!
type: docs
weight: 1830
url: /de/net/aspose.words/editablerange/
---
## EditableRange class

Stellt einen einzelnen bearbeitbaren Bereich dar.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class EditableRange
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend/) { get; } | Ruft den Knoten ab, der das Ende des bearbeitbaren Bereichs darstellt. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart/) { get; } | Ruft den Knoten ab, der den Anfang des bearbeitbaren Bereichs darstellt. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup/) { get; set; } | Gibt einen Alias (oder eine Bearbeitungsgruppe) zurück oder legt ihn fest, der verwendet werden soll, um zu bestimmen, ob der aktuelle Benutzer diesen bearbeitbaren Bereich bearbeiten darf. |
| [Id](../../aspose.words/editablerange/id/) { get; } | Ruft die editierbare Bereichskennung ab. |
| [SingleUser](../../aspose.words/editablerange/singleuser/) { get; set; } | Gibt den einzelnen Benutzer für den bearbeitbaren Bereich zurück oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove/)() | Entfernt den editierbaren Bereich aus dem Dokument. Inhalte innerhalb des editierbaren Bereichs werden nicht entfernt. |

## Bemerkungen

`EditableRange` ist ein "Fassaden"-Objekt, das zwei Knoten kapselt[`EditableRangeStart`](./editablerangestart/) und[`EditableRangeEnd`](./editablerangeend/) in einem Dokumentbaum und ermöglicht das Arbeiten mit einem bearbeitbaren Bereich als einzelnes Objekt.

## Beispiele

Zeigt, wie mit einem bearbeitbaren Bereich gearbeitet wird.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Bearbeitbare Bereiche ermöglichen es uns, Teile geschützter Dokumente zur Bearbeitung offen zu lassen.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Ein wohlgeformter bearbeitbarer Bereich hat einen Startknoten und einen Endknoten.
// Diese Knoten haben übereinstimmende IDs und umfassen bearbeitbare Knoten.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Verschiedene Teile des bearbeitbaren Bereichs sind miteinander verknüpft.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// So können wir auf die Knotentypen jedes Teils zugreifen. Der editierbare Bereich selbst ist kein Knoten,
// sondern eine Entität, die aus einem Anfang, einem Ende und dem darin enthaltenen Inhalt besteht.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Einen bearbeitbaren Bereich entfernen. Alle Knoten innerhalb des Bereichs bleiben erhalten.
editableRange.Remove();
```

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
