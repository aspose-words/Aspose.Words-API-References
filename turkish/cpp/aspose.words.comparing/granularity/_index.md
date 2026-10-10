---
title: "Aspose::Words::Comparing::Granularity enum"
linktitle: "Granularity"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Comparing::Granularity enum. C++'da iki belgeyi karşılaştırırken izlenecek değişikliklerin ayrıntı seviyesini belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.comparing/granularity/
---
## Granularity enum


İki belgeyi karşılaştırırken izlenecek değişikliklerin ayrıntı seviyesini belirtir.

```cpp
enum class Granularity
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| CharLevel | 0 | Karakter seviyesinde değişiklikleri belirtir. |
| WordLevel | 1 | Kelime seviyesinde değişiklikleri belirtir. |


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

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
