---
title: "Aspose::Words::Document::AcceptAllRevisions metodu"
linktitle: "AcceptAllRevisions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::AcceptAllRevisions metodu. C++'ta belgede izlenen tüm değişiklikleri kabul eder."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Belgedeki tüm izlenen değişiklikleri kabul eder.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Örnekler



Belgedeki tüm izleme değişikliklerini nasıl kabul edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Değişiklik izlemeyi etkinleştirerek belgeyi düzenleyin ve birkaç revizyon oluşturun.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Her bir revizyonu dolaşabilir ve belge içinde kabul/reddedebiliriz.
// Her revizyonu kabul etmek istediğimizi biliyorsak, bu metodu çağırarak daha doğrudan yapabiliriz.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
