---
title: Aspose::Words::EditableRangeStart class
linktitle: EditableRangeStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRangeStart class. Represents a start of an editable range in a Word document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words/editablerangestart/
---
## EditableRangeStart class


Represents a start of an editable range in a Word document. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class EditableRangeStart : public Aspose::Words::Node,
                           public Aspose::Words::IDisplaceableByCustomXml,
                           public Aspose::Words::INodeWithAnnotationId
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_EditableRange](./get_editablerange/)() | Gets the facade object that encapsulates this editable range start and end. |
| [get_Id](./get_id/)() const | Specifies the identifier of the editable range. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [EditableRangeStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Id](./set_id/)(int32_t) | Setter for [Aspose::Words::EditableRangeStart::get_Id](./get_id/). |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


A complete editable range in a Word document consists of a [EditableRangeStart](./) and a matching [EditableRangeEnd](../editablerangeend/) with the same Id.

[EditableRangeStart](./) and [EditableRangeEnd](../editablerangeend/) are just markers inside a document that specify where the editable range starts and ends.

Use the [EditableRange](./get_editablerange/) class as a "facade" to work with an editable range as a single object.


Currently editable ranges are supported only at the inline-level, that is inside [Paragraph](../paragraph/), but editable range start and editable range end can be in different paragraphs.
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

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
