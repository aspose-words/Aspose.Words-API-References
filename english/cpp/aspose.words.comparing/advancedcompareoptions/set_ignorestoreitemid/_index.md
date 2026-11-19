---
title: Aspose::Words::Comparing::AdvancedCompareOptions::set_IgnoreStoreItemId method
linktitle: set_IgnoreStoreItemId
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comparing::AdvancedCompareOptions::set_IgnoreStoreItemId method. Specifies whether to ignore difference in StructuredDocumentTag store item Id in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.comparing/advancedcompareoptions/set_ignorestoreitemid/
---
## AdvancedCompareOptions::set_IgnoreStoreItemId method


Specifies whether to ignore difference in [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) store item Id.

```cpp
void Aspose::Words::Comparing::AdvancedCompareOptions::set_IgnoreStoreItemId(bool value)
```

## Remarks

 Default value is **false**. 
## Examples


Shows how to compare SDT with same content but different store item id.

```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document with SDT 1.docx"));
auto docB = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document with SDT 2.docx"));

// Configure options to compare SDT with same content but different store item id.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(docA->get_Revisions()->get_Count(), 8);

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(docA->get_Revisions()->get_Count(), 0);
```
## See Also

* [get_IgnoreStoreItemId](../get_ignorestoreitemid/)

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
