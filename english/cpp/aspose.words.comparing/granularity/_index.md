---
title: Aspose::Words::Comparing::Granularity enum
linktitle: Granularity
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::Granularity enum. Specifies the granularity of changes to track when comparing two documents in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.comparing/granularity/
---
## Granularity enum


Specifies the granularity of changes to track when comparing two documents.

```cpp
enum class Granularity
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| CharLevel | 0 | Specifies changes at the character level. |
| WordLevel | 1 | Specifies changes at the word level. |


## Examples



Shows to specify a granularity while comparing documents. 
```cpp
auto docA = MakeObject<Document>();
auto builderA = MakeObject<DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = MakeObject<Document>();
auto builderB = MakeObject<DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specify whether changes are tracking
// by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
auto compareOptions = MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// The first document's collection of revision groups contains all the differences between documents.
SharedPtr<RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## See Also

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
