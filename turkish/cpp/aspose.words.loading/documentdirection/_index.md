---
title: "Aspose::Words::Loading::DocumentDirection enum"
linktitle: "DocumentDirection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::DocumentDirection enum. C++'ta bir belgede metnin akış yönünü belirtmeye olanak tanır."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.loading/documentdirection/
---
## DocumentDirection enum


Belgedeki metnin akış yönünü belirtmenizi sağlar.

```cpp
enum class DocumentDirection
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| LeftToRight | 0 | Soldan sağa yön. |
| RightToLeft | 1 | Sağdan sola yön. |
| Otomatik | 2 | Yönü otomatik algıla. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
