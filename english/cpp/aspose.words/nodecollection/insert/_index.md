---
title: Insert
second_title: Aspose.Words for C++ API Reference
description: Inserts a node into the collection at the specified index.
type: docs
weight: 92
url: /cpp/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method


Inserts a node into the collection at the specified index.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to insert. |

The node is inserted as a child into the node object from which the collection was created.

If the index is equal to or greater than Count, the node is added at the end of the collection.

If the index is negative and its absolute value is greater than Count, the node is added at the end of the collection.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **ImportNode()** to import the node to the current document. The imported node can then be inserted into the current document.

## Examples




Shows how to work with a [NodeCollection](../). 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add text to the document by inserting Runs using a DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Every invocation of the "Write" method creates a new Run,
// which then appears in the parent Paragraph's RunCollection.
SharedPtr<RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// We can also insert a node into the RunCollection manually.
auto newRun = MakeObject<Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Access individual runs and remove them to remove their text from the document.
SharedPtr<Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(run == nullptr);
ASSERT_FALSE(runs->Contains(run));
```

