---
title: FieldSeparator
second_title: Aspose.Words for C++ API Reference
description: Represents a Word field separator that separates the field code from the field result.
type: docs
weight: 1158
url: /cpp/aspose.words.fields/fieldseparator/
---
## FieldSeparator class


Represents a Word field separator that separates the field code from the field result.

```cpp
class FieldSeparator : public Aspose::Words::Fields::FieldChar
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Returns the type of the field. |
| [get_Font](../../aspose.words/inline/get_font/)() | Provides access to the font formatting of this object. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns true if this node can contain other nodes. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Gets or sets whether the parent field is locked (should not recalculate its result). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns **FieldSeparator**. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | Returns a field for the field char. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Gets the special character that this node represents. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/). |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

[FieldSeparator](./) is an inline-level node and represented by the [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) control character in the document.

[FieldSeparator](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the **InsertField()** method.

## Examples




Shows how to work with a collection of fields. 
```cpp
void FieldCollection_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder->InsertField(u" TIME ");
    builder->InsertField(u" REVNUM ");
    builder->InsertField(u" AUTHOR  \"John Doe\" ");
    builder->InsertField(u" SUBJECT \"My Subject\" ");
    builder->InsertField(u" QUOTE \"Hello world!\" ");
    doc->UpdateFields();

    SharedPtr<FieldCollection> fields = doc->get_Range()->get_Fields();

    ASSERT_EQ(6, fields->get_Count());

    // Iterate over the field collection, and print contents and type
    // of every field using a custom visitor implementation.
    auto fieldVisitor = MakeObject<ExField::FieldVisitor>();

    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<Field>>> fieldEnumerator = fields->GetEnumerator();
        while (fieldEnumerator->MoveNext())
        {
            if (fieldEnumerator->get_Current() != nullptr)
            {
                fieldEnumerator->get_Current()->get_Start()->Accept(fieldVisitor);
                if (fieldEnumerator->get_Current()->get_Separator() != nullptr)
                {
                    fieldEnumerator->get_Current()->get_Separator()->Accept(fieldVisitor);
                }
                fieldEnumerator->get_Current()->get_End()->Accept(fieldVisitor);
            }
            else
            {
                std::cout << "There are no fields in the document." << std::endl;
            }
        }
    }

    std::cout << fieldVisitor->GetText() << std::endl;
}

class FieldVisitor : public DocumentVisitor
{
public:
    FieldVisitor()
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitFieldStart(SharedPtr<FieldStart> fieldStart) override
    {
        mBuilder->AppendLine(String(u"Found field: ") + System::ObjectExt::ToString(fieldStart->get_FieldType()));
        mBuilder->AppendLine(String(u"\tField code: ") + fieldStart->GetField()->GetFieldCode());
        mBuilder->AppendLine(String(u"\tDisplayed as: ") + fieldStart->GetField()->get_Result());

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldSeparator(SharedPtr<FieldSeparator> fieldSeparator) override
    {
        mBuilder->AppendLine(String(u"\tFound separator: ") + fieldSeparator->GetText());

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        mBuilder->AppendLine(String(u"End of field: ") + System::ObjectExt::ToString(fieldEnd->get_FieldType()));

        return VisitorAction::Continue;
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;
};
```

