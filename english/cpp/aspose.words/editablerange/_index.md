---
title: EditableRange
second_title: Aspose.Words for C++ API Reference
description: Represents a single editable range. To learn more, visit the  documentation article.
type: docs
weight: 300
url: /cpp/aspose.words/editablerange/
---
## EditableRange class


Represents a single editable range. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class EditableRange : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Gets the node that represents the end of the editable range. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Gets the node that represents the start of the editable range. |
| [get_EditorGroup](./get_editorgroup/)() | Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [get_Id](./get_id/)() | Gets the editable range identifier. |
| [get_SingleUser](./get_singleuser/)() | Returns or sets the single user for editable range. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes the editable range from the document. Does not remove content inside the editable range. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Setter for [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Setter for [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Remarks


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## Examples



Shows how to work with an editable range. 
```cpp
auto doc = MakeObject<Document>();
doc->Protect(ProtectionType::ReadOnly, u"MyPassword");

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(String(u"Hello world! Since we have set the document's protection level to read-only,") +
                 u" we cannot edit this paragraph without the password.");

// Editable ranges allow us to leave parts of protected documents open for editing.
SharedPtr<EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
SharedPtr<EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// A well-formed editable range has a start node, and end node.
// These nodes have matching IDs and encompass editable nodes.
SharedPtr<EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Different parts of the editable range link to each other.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// We can access the node types of each part like this. The editable range itself is not a node,
// but an entity which consists of a start, an end, and their enclosed contents.
ASSERT_EQ(NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(ArtifactsDir + u"EditableRange.CreateAndRemove.docx");

// Remove an editable range. All the nodes that were inside the range will remain intact.
editableRange->Remove();
```


Shows how to limit the editing rights of editable ranges to a specific group/user. 
```cpp
void Visitor()
{
    auto doc = MakeObject<Document>();
    doc->Protect(ProtectionType::ReadOnly, u"MyPassword");

    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->Writeln(String(u"Hello world! Since we have set the document's protection level to read-only,") +
                     u" we cannot edit this paragraph without the password.");

    // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
    // There are two mutually exclusive ways to narrow down the list of allowed editors.
    // 1 -  Specify a user:
    SharedPtr<EditableRange> editableRange = builder->StartEditableRange()->get_EditableRange();
    editableRange->set_SingleUser(u"john.doe@myoffice.com");
    builder->Writeln(String::Format(u"This paragraph is inside the first editable range, can only be edited by {0}.", editableRange->get_SingleUser()));
    builder->EndEditableRange();

    ASSERT_EQ(EditorType::Unspecified, editableRange->get_EditorGroup());

    // 2 -  Specify a group that allowed users are associated with:
    editableRange = builder->StartEditableRange()->get_EditableRange();
    editableRange->set_EditorGroup(EditorType::Administrators);
    builder->Writeln(String::Format(u"This paragraph is inside the first editable range, can only be edited by {0}.", editableRange->get_EditorGroup()));
    builder->EndEditableRange();

    ASSERT_EQ(String::Empty, editableRange->get_SingleUser());

    builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Print details and contents of every editable range in the document.
    auto editableRangePrinter = MakeObject<ExEditableRange::EditableRangePrinter>();

    doc->Accept(editableRangePrinter);

    std::cout << editableRangePrinter->ToText() << std::endl;
}

class EditableRangePrinter : public DocumentVisitor
{
public:
    EditableRangePrinter() : mInsideEditableRange(false)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String ToText()
    {
        return mBuilder->ToString();
    }

    void Reset()
    {
        mBuilder->Clear();
        mInsideEditableRange = false;
    }

    VisitorAction VisitEditableRangeStart(SharedPtr<EditableRangeStart> editableRangeStart) override
    {
        mBuilder->AppendLine(u" -- Editable range found! -- ");
        mBuilder->AppendLine(String(u"\tID:\t\t") + editableRangeStart->get_Id());
        if (editableRangeStart->get_EditableRange()->get_SingleUser() == String::Empty)
        {
            mBuilder->AppendLine(String(u"\tGroup:\t") + System::ObjectExt::ToString(editableRangeStart->get_EditableRange()->get_EditorGroup()));
        }
        else
        {
            mBuilder->AppendLine(String(u"\tUser:\t") + editableRangeStart->get_EditableRange()->get_SingleUser());
        }
        mBuilder->AppendLine(u"\tContents:");

        mInsideEditableRange = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitEditableRangeEnd(SharedPtr<EditableRangeEnd> editableRangeEnd) override
    {
        mBuilder->AppendLine(u" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction::Continue;
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mInsideEditableRange)
        {
            mBuilder->AppendLine(String(u"\t\"") + run->get_Text() + u"\"");
        }

        return VisitorAction::Continue;
    }

private:
    bool mInsideEditableRange;
    SharedPtr<System::Text::StringBuilder> mBuilder;
};
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
