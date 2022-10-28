---
title: get_Granularity
second_title: Aspose.Words for C++ API Reference
description: Specifies whether changes are tracked by character or by word. Default value is WordLevel.
type: docs
weight: 14
url: /cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions.get_Granularity method


Specifies whether changes are tracked by character or by word. Default value is **WordLevel**.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


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

