---
title: JoinRunsWithSameFormatting
second_title: Aspose.Words for C++ API Reference
description: Joins runs with same formatting in all paragraphs of the document.
type: docs
weight: 807
url: /cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Joins runs with same formatting in all paragraphs of the document.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
## Remarks


This is an optimization method. Some documents contain adjacent runs with same formatting. Usually this occurs if a document was intensively edited manually. You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../paragraph/) node in the document for adjacent [Run](../../run/) nodes having identical properties. It ignores unique identifiers used to track editing sessions of run creation and modification. First run in every joining sequence accumulates all text. Remaining runs are deleted from the document.

## Examples



Shows how to join runs in a document to reduce unneeded runs. 
```cpp
// Open a document that contains adjacent runs of text with identical formatting,
// which commonly occurs if we edit the same paragraph multiple times in Microsoft Word.
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// If any number of these runs are adjacent with identical formatting,
// then the document may be simplified.
ASSERT_EQ(317, doc->GetChildNodes(NodeType::Run, true)->get_Count());

// Combine such runs with this method and verify the number of run joins that will take place.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// The number of joins and the number of runs we have after the join
// should add up the number of runs we had initially.
ASSERT_EQ(196, doc->GetChildNodes(NodeType::Run, true)->get_Count());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
