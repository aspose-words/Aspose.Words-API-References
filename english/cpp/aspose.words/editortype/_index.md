---
title: EditorType
second_title: Aspose.Words for C++ API Reference
description: Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document.
type: docs
weight: 1132
url: /cpp/aspose.words/editortype/
---
## EditorType enum


Specifies the set of possible aliases (or editing groups) which can be used as aliases to determine if the current user shall be allowed to edit a single range defined by an editable range within a document.

```cpp
enum class EditorType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unspecified | 0 | Means that editor type is not specified. |
| Administrators | 1 | Specifies that users associated with the Administrators group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Contributors | 2 | Specifies that users associated with the Contributors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Current | 3 | Specifies that users associated with the Current group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Editors | 4 | Specifies that users associated with the Editors group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Everyone | 5 | Specifies that all users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| None | 6 | Specifies that none of the users that open the document shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Owners | 7 | Specifies that users associated with the Owners group shall be allowed to edit editable ranges using this editing type when document protection is enabled. |
| Default | n/a | Same as [Unspecified](./). |


## Examples



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
