---
title: Aspose::Words::NodeList::GetEnumerator method
linktitle: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeList::GetEnumerator method. Provides a simple "foreach" style iteration over the collection of nodes in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/nodelist/getenumerator/
---
## NodeList::GetEnumerator method


Provides a simple "foreach" style iteration over the collection of nodes.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Node>>> Aspose::Words::NodeList::GetEnumerator() override
```


### ReturnValue

An IEnumerator.

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

## See Also

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
