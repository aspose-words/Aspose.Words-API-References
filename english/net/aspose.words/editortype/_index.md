---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: Aspose.Words for .NET
description: Aspose.Words.EditorType enum. Specifies the set of possible aliases or editing groups which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document in C#.
type: docs
weight: 1420
url: /net/aspose.words/editortype/
---
## EditorType enumeration

Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document.

```csharp
public enum EditorType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unspecified | `0` | Means that editor type is not specified. |
| Administrators | `1` | Specifies that users associated with the Administrators group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Contributors | `2` | Specifies that users associated with the Contributors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Current | `3` | Specifies that users associated with the Current group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Editors | `4` | Specifies that users associated with the Editors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Everyone | `5` | Specifies that all users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| None | `6` | Specifies that none of the users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Owners | `7` | Specifies that users associated with the Owners group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Default | `0` | Same as Unspecified. |

## Examples

Shows how to limit the editing rights of editable ranges to a specific group/user.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
    // There are two mutually exclusive ways to narrow down the list of allowed editors.
    // 1 -  Specify a user:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 -  Specify a group that allowed users are associated with:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Print details and contents of every editable range in the document.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Collects properties and contents of visited editable ranges in a string.
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
    /// Called when an EditableRangeStart node is encountered in the document.
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
    /// Called when an EditableRangeEnd node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
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

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
