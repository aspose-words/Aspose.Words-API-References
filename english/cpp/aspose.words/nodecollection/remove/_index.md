---
title: Aspose::Words::NodeCollection::Remove method
linktitle: Remove
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::Remove method. Removes the node from the collection and from the document in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/nodecollection/remove/
---
## NodeCollection::Remove method


Removes the node from the collection and from the document.

```cpp
void Aspose::Words::NodeCollection::Remove(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Type | Description |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to remove. |

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

## See Also

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
