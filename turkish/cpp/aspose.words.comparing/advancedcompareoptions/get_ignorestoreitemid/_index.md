---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId yöntemi"
linktitle: "get_IgnoreStoreItemId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId yöntemi. StructuredDocumentTag depolama öğesi kimliğindeki farkı C++'ta yok sayıp saymayacağını belirtir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


StructuredDocumentTag depolama öğesi kimliğindeki farkı göz ardı edip etmeyeceğini belirtir.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## Örnekler



Aynı içeriğe sahip ancak farklı depolama öğesi kimliğine sahip SDT'yi nasıl karşılaştıracağınızı gösterir.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Aynı içeriğe sahip ancak farklı depolama öğesi kimliğine sahip SDT'yi karşılaştırmak için seçenekleri yapılandırın.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## Ayrıca Bakınız

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
