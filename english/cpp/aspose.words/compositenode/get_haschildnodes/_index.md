---
title: get_HasChildNodes
second_title: Aspose.Words for C++ API Reference
description: Returns true if this node has any child nodes.
type: docs
weight: 53
url: /cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode.get_HasChildNodes method


Returns true if this node has any child nodes.

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## Examples




Shows how to combine the rows from two tables into one. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

// Below are two ways of getting a table from a document.
// 1 -  From the "Tables" collection of a Body node:
SharedPtr<Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Using the "GetChild" method:
auto secondTable = System::DynamicCast<Table>(doc->GetChild(NodeType::Table, 1, true));

// Append all rows from the current table to the next.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Remove the empty table container.
secondTable->Remove();

doc->Save(ArtifactsDir + u"Table.CombineTables.docx");
```

