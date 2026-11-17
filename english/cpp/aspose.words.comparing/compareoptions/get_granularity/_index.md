---
title: Aspose::Words::Comparing::CompareOptions::get_Granularity method
linktitle: get_Granularity
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::CompareOptions::get_Granularity method. Specifies whether changes are tracked by character or by word in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


Specifies whether changes are tracked by character or by word.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## Examples



Shows to specify a granularity while comparing documents. 
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specify whether changes are tracking
// by character ('Granularity.CharLevel'), or by word ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// The first document's collection of revision groups contains all the differences between documents.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## See Also

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
