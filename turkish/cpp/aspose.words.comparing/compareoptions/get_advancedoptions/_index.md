---
title: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions metodu"
linktitle: "get_AdvancedOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions metodu. C++'ta daha kesin karşılaştırma çıktısı üretmeye yardımcı olabilecek gelişmiş karşılaştırma seçeneklerini belirtir."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.comparing/compareoptions/get_advancedoptions/
---
## CompareOptions::get_AdvancedOptions method


Daha kesin karşılaştırma çıktısı üretmeye yardımcı olabilecek gelişmiş karşılaştırma seçeneklerini belirtir.

```cpp
const System::SharedPtr<Aspose::Words::Comparing::AdvancedCompareOptions> & Aspose::Words::Comparing::CompareOptions::get_AdvancedOptions() const
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

* Class [AdvancedCompareOptions](../../advancedcompareoptions/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
