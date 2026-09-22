---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection yöntemi"
linktitle: "get_DocumentDirection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection yöntemi. Belge yönünü alır veya ayarlar. Varsayılan değer C++'da LeftToRight'tir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


Belge yönünü alır veya ayarlar. Varsayılan değer [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


## Örnekler



Düz metin belgesinin metin yönünün nasıl algılanacağını gösterir.
```cpp
// "TxtLoadOptions" nesnesi oluşturun, bunu bir belgenin yapıcısına geçirebiliriz
// düz metin belgesini nasıl yüklediğimizi değiştirmek için.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// "DocumentDirection" özelliğini "DocumentDirection.Auto" olarak ayarlayın, otomatik olarak algılar
// Aspose.Words'ın düz metinden yüklediği her paragrafın yönünü.
// Her paragrafın "Bidi" özelliği yönünü saklayacaktır.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// İbranice metni sağdan sola olarak algıla.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// İngilizce metni sağdan sola olarak algıla.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Ayrıca Bakınız

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
