---
title: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId yöntemi"
linktitle: "get_IgnoreDmlUniqueId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId yöntemi. C++'de DrawingML benzersiz kimliğindeki farkı göz ardı edip etmeyeceğini belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.comparing/advancedcompareoptions/get_ignoredmluniqueid/
---
## AdvancedCompareOptions::get_IgnoreDmlUniqueId method


DrawingML benzersiz kimliğindeki farkı göz ardı edip etmeyeceğini belirtir.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId() const
```


## Örnekler



DML benzersiz kimliğini göz ardı ederek belgelerin nasıl karşılaştırılacağını gösterir.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID original.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DML unique ID compare.docx");

// Varsayılan olarak, Aspose.Words DML'nin benzersiz kimliğini göz ardı etmez ve revizyon sayısı 2 idi.
// Eğer DML'nin benzersiz kimliğini göz ardı ediyorsak, revizyon sayısı 0 olur.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreDmlUniqueId(isIgnoreDmlUniqueId);

docA->Compare(docB, u"Aspose.Words", System::DateTime::get_Now(), compareOptions);

ASSERT_EQ(isIgnoreDmlUniqueId ? 0 : 2, docA->get_Revisions()->get_Count());
```

## Ayrıca Bakınız

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
