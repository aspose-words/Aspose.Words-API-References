---
title: Aspose::Words::Comparing::AdvancedCompareOptions::get_CompareListDefinitions method
linktitle: get_CompareListDefinitions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::AdvancedCompareOptions::get_CompareListDefinitions method. Specifies whether list definition contents are compared instead of list definition Ids in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.comparing/advancedcompareoptions/get_comparelistdefinitions/
---
## AdvancedCompareOptions::get_CompareListDefinitions method


Specifies whether list definition contents are compared instead of list definition Ids.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_CompareListDefinitions() const
```


## Examples



Shows how to control whether list definition content will be compared during document comparison. 
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->get_ListFormat()->ApplyNumberDefault();
builderA->Writeln(u"Item 1");
builderA->Writeln(u"Item 2");
builderA->get_ListFormat()->RemoveNumbers();

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->get_ListFormat()->ApplyBulletDefault();
builderB->Writeln(u"Item 1");
builderB->Writeln(u"Item 2");
builderB->get_ListFormat()->RemoveNumbers();

// Compare documents with CompareListDefinitions enabled.
auto options = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
options->get_AdvancedOptions()->set_CompareListDefinitions(isCompareListDefinitions);
docA->Compare(docB, u"test", System::DateTime::get_Now(), options);
```

## See Also

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
