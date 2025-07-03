---
title: Aspose::Words::NodeCollection::Contains method
linktitle: Contains
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection::Contains method. Determines whether a node is in the collection in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Determines whether a node is in the collection.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parameter | Type | Description |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to locate. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Remarks


This method performs a linear search; therefore, the average execution time is proportional to [Count](../get_count/).

## Examples



Shows how to work with a [NodeCollection](../). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add text to the document by inserting Runs using a DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Every invocation of the "Write" method creates a new Run,
// which then appears in the parent Paragraph's RunCollection.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// We can also insert a node into the RunCollection manually.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Access individual runs and remove them to remove their text from the document.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## See Also

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
