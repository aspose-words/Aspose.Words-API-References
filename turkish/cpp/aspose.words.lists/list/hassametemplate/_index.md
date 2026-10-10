---
title: "Aspose::Words::Lists::List::HasSameTemplate yöntemi"
linktitle: "HasSameTemplate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::List::HasSameTemplate yöntemi. Mevcut liste ve verilen listenin aynı şablondan oluşturulmuş olması durumunda true döndürür C++ içinde."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.lists/list/hassametemplate/
---
## List::HasSameTemplate method


Mevcut liste ve verilen listenin aynı şablondan oluşturulmuş olması durumunda true döndürür.

```cpp
bool Aspose::Words::Lists::List::HasSameTemplate(const System::SharedPtr<Aspose::Words::Lists::List> &other)
```


## Örnekler



Aynı ListDefId'ye sahip listelerin nasıl tanımlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Different lists.docx");

ASSERT_TRUE(doc->get_Lists()->idx_get(0)->HasSameTemplate(doc->get_Lists()->idx_get(1)));
ASSERT_FALSE(doc->get_Lists()->idx_get(1)->HasSameTemplate(doc->get_Lists()->idx_get(2)));
```

## Ayrıca Bakınız

* Class [List](../)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
