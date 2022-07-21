---
title: EditableRangeStart
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt den Beginn eines bearbeitbaren Bereichs in einem Word-Dokument dar.
type: docs
weight: 1290
url: /de/net/aspose.words/editablerangestart/
---
## EditableRangeStart class

Stellt den Beginn eines bearbeitbaren Bereichs in einem Word-Dokument dar.

```csharp
public sealed class EditableRangeStart : Node
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [EditableRange](../../aspose.words/editablerangestart/editablerange) { get; } | Ruft das Fassadenobjekt ab, das den Anfang und das Ende dieses bearbeitbaren Bereichs kapselt. |
| [Id](../../aspose.words/editablerangestart/id) { get; set; } | Gibt die Kennung des editierbaren Bereichs an. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/editablerangestart/nodetype) { get; } | gibt zurückEditableRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/editablerangestart/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| virtual [GetText](../../aspose.words/node/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Ein vollständig bearbeitbarer Bereich in einem Word-Dokument besteht aus a[`EditableRangeStart`](../editablerangestart) und ein passendes[`EditableRangeEnd`](../editablerangeend) mit der gleichen ID.

[`EditableRangeStart`](../editablerangestart) und[`EditableRangeEnd`](../editablerangeend) sind nur Markierungen innerhalb eines document , die angeben, wo der bearbeitbare Bereich beginnt und endet.

Verwenden Sie die[`EditableRange`](./editablerange)Klasse als "Fassade", um mit einem bearbeitbaren Bereich als einzelnes Objekt zu arbeiten.

Derzeit bearbeitbare Bereiche werden nur auf der Inline-Ebene unterstützt, also innerhalb[`Paragraph`](../paragraph), aber bearbeitbarer Bereichsanfang und bearbeitbares Bereichsende können sich in unterschiedlichen Absätzen befinden.

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

* class [Node](../node)
* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
