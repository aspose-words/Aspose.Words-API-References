---
title: Aspose::Words::NodeList::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeList::idx_get method. Retrieves a node at the given index in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


Retrieves a node at the given index.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the list of nodes. |
## Remarks


The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples



Shows how to use XPaths to navigate a [NodeList](../). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert some nodes with a DocumentBuilder.
builder->Writeln(u"Hello world!");

builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Our document contains three Run nodes.
System::SharedPtr<Aspose::Words::NodeList> nodeList = doc->SelectNodes(u"//Run");

ASSERT_EQ(3, nodeList->get_Count());
ASSERT_TRUE(nodeList->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return n->GetText().Trim() == u"Hello world!";
}))));
ASSERT_TRUE(nodeList->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return n->GetText().Trim() == u"Cell 1";
}))));
ASSERT_TRUE(nodeList->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return n->GetText().Trim() == u"Cell 2";
}))));

// Use a double forward slash to select all Run nodes
// that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
nodeList = doc->SelectNodes(u"//Table//Run");

ASSERT_EQ(2, nodeList->get_Count());
ASSERT_TRUE(nodeList->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return n->GetText().Trim() == u"Cell 1";
}))));
ASSERT_TRUE(nodeList->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return n->GetText().Trim() == u"Cell 2";
}))));

// Single forward slashes specify direct descendant relationships,
// which we skipped when we used double slashes.
ASPOSE_ASSERT_EQ(doc->SelectNodes(u"//Table//Run"), doc->SelectNodes(u"//Table/Row/Cell/Paragraph/Run"));

// Access the shape that contains the image we inserted.
nodeList = doc->SelectNodes(u"//Shape");

ASSERT_EQ(1, nodeList->get_Count());

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(nodeList->idx_get(0));
ASSERT_TRUE(shape->get_HasImage());
```

## See Also

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
