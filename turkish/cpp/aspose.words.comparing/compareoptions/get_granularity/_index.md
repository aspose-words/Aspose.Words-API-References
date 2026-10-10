---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity yöntemi"
linktitle: "get_Granularity"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity yöntemi. C++'ta değişikliklerin karakter bazında mı yoksa kelime bazında mı izleneceğini belirtir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


Değişikliklerin karakter bazında mı yoksa kelime bazında mı izleneceğini belirtir.

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## Örnekler



Belgeleri karşılaştırırken bir incelik düzeyi belirtmeyi gösterir.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Değişikliklerin izlenip izlenmeyeceğini belirtin.
// karaktere göre ('Granularity.CharLevel'), ya da kelimeye göre ('Granularity.WordLevel').
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// İlk belgenin revizyon grupları koleksiyonu, belgeler arasındaki tüm farkları içerir.
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## Ayrıca Bakınız

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
