---
title: Aspose::Words::NodeList class
linktitle: NodeList
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeList class. Represents a collection of nodes matching an XPath query executed using the SelectNodes() method. To learn more, visit the  documentation article in C++.'
type: docs
weight: 45000
url: /cpp/aspose.words/nodelist/
---
## NodeList class


Represents a collection of nodes matching an XPath query executed using the [SelectNodes()](../) method. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class NodeList : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methods

| Method | Description |
| --- | --- |
| [get_Count](./get_count/)() const | Gets the number of nodes in the list. |
| [GetEnumerator](./getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) const | Retrieves a node at the given index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeList](./nodelist/)(const System::SharedPtr\<Aspose::Words::NodeCollection\>\&) |  |
| [ToArray](./toarray/)() const | Copies all nodes from the collection to a new array of nodes. |
| static [Type](./type/)() |  |
## Remarks


[NodeList](./) is returned by [SelectNodes()](../) and contains a collection of nodes matching the XPath query.

[NodeList](./) supports indexed access and iteration.


Treat the [NodeList](./) collection as a "snapshot" collection. [NodeList](./) starts as a "live" collection because the nodes are not actually retrieved when the XPath query is run. The nodes are only retrieved upon access and at this time the node and all nodes that precede it are cached forming a "snapshot" collection.
## Examples



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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
