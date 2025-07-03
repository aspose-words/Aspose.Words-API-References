---
title: Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId method
linktitle: get_IgnoreDmlUniqueId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId method. Specifies whether to ignore difference in DrawingML unique Id in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


Specifies whether to ignore difference in DrawingML unique Id.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
```


## Examples



Shows how to compare documents ignoring DML unique ID. 
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
// If we are ignoring DML's unique ID, and revisions count were 0.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## See Also

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
