---
title: Aspose::Words::Fields::FieldStart class
linktitle: FieldStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldStart class. Represents a start of a Word field in a document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 95000
url: /cpp/aspose.words.fields/fieldstart/
---
## FieldStart class


Represents a start of a Word field in a document. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldStart : public Aspose::Words::Fields::FieldChar
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FieldData](./get_fielddata/)() const | Gets custom field data which is associated with the field. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Returns the type of the field. |
| [get_Font](../../aspose.words/inline/get_font/)() | Provides access to the font formatting of this object. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Gets or sets whether the parent field is locked (should not recalculate its result). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [FieldStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | Returns a field for the field char. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Gets the special character that this node represents. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/). |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


[FieldStart](./) is an inline-level node and represented by the [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) control character in the document.

[FieldStart](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [InsertField()](../) method.

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


Shows how to find all hyperlinks in a Word document, and then change their URLs and display names. 
```cpp
#include <cstdint>
#include <Aspose.Words.Cpp/CompositeNode.h>
#include <Aspose.Words.Cpp/Document.h>
#include <Aspose.Words.Cpp/Fields/FieldStart.h>
#include <Aspose.Words.Cpp/Fields/FieldType.h>
#include <Aspose.Words.Cpp/Node.h>
#include <Aspose.Words.Cpp/NodeList.h>
#include <Aspose.Words.Cpp/NodeType.h>
#include <Aspose.Words.Cpp/Run.h>
#include <Aspose.Words.Cpp/Saving/SaveOutputParameters.h>
#include <system/collections/ienumerable.h>
#include <system/enumerator_adapter.h>
#include <system/exceptions.h>
#include <system/linq/enumerable.h>
#include <system/object_ext.h>
#include <system/text/regularexpressions/group.h>
#include <system/text/regularexpressions/group_collection.h>
#include <system/text/regularexpressions/match.h>
#include <system/text/regularexpressions/regex.h>
#include <system/text/string_builder.h>

#include "ApiExampleBase.h"

using System::ArrayPtr;
using System::MakeArray;
using System::MakeObject;
using System::SharedPtr;
using System::String;

using namespace Aspose::Words;
using namespace Aspose::Words::Fields;

namespace ApiExamples {

class Hyperlink : public System::Object
{
public:
    String get_Name()
    {
        return GetTextSameParent(mFieldSeparator, mFieldEnd);
    }

    void set_Name(String value)
    {
        // Hyperlink display name is stored in the field result, which is a Run
        // node between field separator and field end.
        auto fieldResult = System::DynamicCast<Run>(mFieldSeparator->get_NextSibling());
        fieldResult->set_Text(value);

        // If the field result consists of more than one run, delete these runs.
        RemoveSameParent(fieldResult->get_NextSibling(), mFieldEnd);
    }

    String get_Target()
    {
        return mTarget;
    }

    void set_Target(String value)
    {
        mTarget = value;
        UpdateFieldCode();
    }

    bool get_IsLocal()
    {
        return mIsLocal;
    }

    void set_IsLocal(bool value)
    {
        mIsLocal = value;
        UpdateFieldCode();
    }

    Hyperlink(SharedPtr<FieldStart> fieldStart) : mIsLocal(false)
    {
        if (fieldStart == nullptr)
        {
            throw System::ArgumentNullException(u"fieldStart");
        }
        if (fieldStart->get_FieldType() != FieldType::FieldHyperlink)
        {
            throw System::ArgumentException(u"Field start type must be FieldHyperlink.");
        }

        mFieldStart = fieldStart;

        // Find the field separator node.
        mFieldSeparator = FindNextSibling(mFieldStart, NodeType::FieldSeparator);
        if (mFieldSeparator == nullptr)
        {
            throw System::InvalidOperationException(u"Cannot find field separator.");
        }

        // Normally, we can always find the field's end node, but the example document
        // contains a paragraph break inside a hyperlink, which puts the field end
        // in the next paragraph. It will be much more complicated to handle fields which span several
        // paragraphs correctly. In this case allowing field end to be null is enough.
        mFieldEnd = FindNextSibling(mFieldSeparator, NodeType::FieldEnd);

        // Field code looks something like "HYPERLINK "http:\\www.myurl.com"", but it can consist of several runs.
        String fieldCode = GetTextSameParent(mFieldStart->get_NextSibling(), mFieldSeparator);
        SharedPtr<System::Text::RegularExpressions::Match> match = gRegex->Match(fieldCode.Trim());

        // The hyperlink is local if \l is present in the field code.
        mIsLocal = match->get_Groups()->idx_get(1)->get_Length() > 0;
        mTarget = match->get_Groups()->idx_get(2)->get_Value();
    }

private:
    SharedPtr<Node> mFieldStart;
    SharedPtr<Node> mFieldSeparator;
    SharedPtr<Node> mFieldEnd;
    bool mIsLocal;
    String mTarget;
    static SharedPtr<System::Text::RegularExpressions::Regex> gRegex;

    void UpdateFieldCode()
    {
        // A field's field code is in a Run node between the field's start node and field separator.
        auto fieldCode = System::DynamicCast<Run>(mFieldStart->get_NextSibling());
        fieldCode->set_Text(String::Format(u"HYPERLINK {0}\"{1}\"", ((mIsLocal) ? String(u"\\l ") : String(u"")), mTarget));

        // If the field code consists of more than one run, delete these runs.
        RemoveSameParent(fieldCode->get_NextSibling(), mFieldSeparator);
    }

    static SharedPtr<Node> FindNextSibling(SharedPtr<Node> startNode, NodeType nodeType)
    {
        for (SharedPtr<Node> node = startNode; node != nullptr; node = node->get_NextSibling())
        {
            if (node->get_NodeType() == nodeType)
            {
                return node;
            }
        }

        return nullptr;
    }

    static String GetTextSameParent(SharedPtr<Node> startNode, SharedPtr<Node> endNode)
    {
        if ((endNode != nullptr) && (startNode->get_ParentNode() != endNode->get_ParentNode()))
        {
            throw System::ArgumentException(u"Start and end nodes are expected to have the same parent.");
        }

        auto builder = MakeObject<System::Text::StringBuilder>();
        for (SharedPtr<Node> child = startNode; !System::ObjectExt::Equals(child, endNode); child = child->get_NextSibling())
        {
            builder->Append(child->GetText());
        }

        return builder->ToString();
    }

    static void RemoveSameParent(SharedPtr<Node> startNode, SharedPtr<Node> endNode)
    {
        if (endNode != nullptr && startNode->get_ParentNode() != endNode->get_ParentNode())
        {
            throw System::ArgumentException(u"Start and end nodes are expected to have the same parent.");
        }

        SharedPtr<Node> curChild = startNode;
        while ((curChild != nullptr) && (curChild != endNode))
        {
            SharedPtr<Node> nextChild = curChild->get_NextSibling();
            curChild->Remove();
            curChild = nextChild;
        }
    }
};

class ExReplaceHyperlinks : public ApiExampleBase

public:
    void Fields()
    {
        auto doc = MakeObject<Document>(MyDir + u"Hyperlinks.docx");

        // Hyperlinks in a Word documents are fields. To begin looking for hyperlinks, we must first find all the fields.
        // Use the "SelectNodes" method to find all the fields in the document via an XPath.
        SharedPtr<NodeList> fieldStarts = doc->SelectNodes(u"//FieldStart");

        for (const auto& fieldStart : System::IterateOver(fieldStarts->LINQ_OfType<SharedPtr<FieldStart>>()))
        {
            if (fieldStart->get_FieldType() == FieldType::FieldHyperlink)
            {
                auto hyperlink = MakeObject<Hyperlink>(fieldStart);

                // Hyperlinks that link to bookmarks do not have URLs.
                if (hyperlink->get_IsLocal())
                {
                    continue;
                }

                // Give each URL hyperlink a new URL and name.
                hyperlink->set_Target(NewUrl);
                hyperlink->set_Name(NewName);
            }
        }

        doc->Save(ArtifactsDir + u"ReplaceHyperlinks.Fields.docx");
    }

    static const String NewUrl;
    static const String NewName;
};

} // namespace ApiExamples
```

## See Also

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
