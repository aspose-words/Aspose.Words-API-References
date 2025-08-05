---
title: Aspose::Words::CompositeNode::SelectNodes method
linktitle: SelectNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::SelectNodes method. Selects a list of nodes matching the XPath expression in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words/compositenode/selectnodes/
---
## CompositeNode::SelectNodes method


Selects a list of nodes matching the XPath expression.

```cpp
System::SharedPtr<Aspose::Words::NodeList> Aspose::Words::CompositeNode::SelectNodes(const System::String &xpath)
```


| Parameter | Type | Description |
| --- | --- | --- |
| xpath | const System::String\& | The XPath expression. |

### ReturnValue

A list of nodes matching the XPath query.
## Remarks


Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

## Examples



Shows how to select certain nodes by using an XPath expression. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// This expression will extract all paragraph nodes,
// which are descendants of any table node in the document.
System::SharedPtr<Aspose::Words::NodeList> nodeList = doc->SelectNodes(u"//Table//Paragraph");

// Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
int32_t index = 0;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Node>>> e = nodeList->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << System::String::Format(u"Table paragraph index {0}, contents: \"{1}\"", index++, e->get_Current()->GetText().Trim()) << std::endl;
    }
}

// This expression will select any paragraphs that are direct children of any Body node in the document.
nodeList = doc->SelectNodes(u"//Body/Paragraph");

// We can treat the list as an array.
ASSERT_EQ(4, nodeList->ToArray()->get_Length());

// Use SelectSingleNode to select the first result of the same expression as above.
System::SharedPtr<Aspose::Words::Node> node = doc->SelectSingleNode(u"//Body/Paragraph");

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::Paragraph>(), System::ObjectExt::GetType(node));
```


Shows how to use an XPath expression to test whether a node is inside a field. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Mail merge destination - Northwind employees.docx");

// The NodeList that results from this XPath expression will contain all nodes we find inside a field.
// However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
// Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
System::SharedPtr<Aspose::Words::NodeList> resultList = doc->SelectNodes(u"//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// Check if the specified run is one of the nodes that are inside the field.
std::cout << System::String::Format(u"Contents of the first Run node that's part of a field: {0}", resultList->LINQ_First(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return n->get_NodeType() == Aspose::Words::NodeType::Run;
})))->GetText().Trim()) << std::endl;
```

## See Also

* Class [NodeList](../../nodelist/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
