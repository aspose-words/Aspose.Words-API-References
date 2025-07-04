---
title: Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId method
linktitle: get_IgnoreStoreItemId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId method. Specifies whether to ignore difference in StructuredDocumentTag store item Id in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


Specifies whether to ignore difference in StructuredDocumentTag store item Id.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Examples



Shows how to compare SDT with same content but different store item id. 
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Configure options to compare SDT with same content but different store item id.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## See Also

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
