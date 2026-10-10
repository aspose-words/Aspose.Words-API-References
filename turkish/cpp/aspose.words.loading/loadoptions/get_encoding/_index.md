---
title: "Aspose::Words::Loading::LoadOptions::get_Encoding yöntemi"
linktitle: "get_Encoding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_Encoding yöntemi. Belge içinde kodlama belirtilmemişse, bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. Null olabilir. Varsayılan değer C++'da null'dur."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Belge içinde kodlama belirtilmemişse bir HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar. **null** olabilir. Varsayılan **null**'dır.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Açıklamalar


Bu özellik yalnızca HTML, TXT veya CHM belgeleri yüklenirken kullanılır.

Belge içinde kodlama belirtilmemiş ve bu özellik **null** ise, sistem kodlamayı otomatik olarak tespit etmeye çalışacaktır.

## Örnekler



Bir belgeyi açmak için kullanılacak kodlamayı nasıl ayarlayacağınızı gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// LoadOptions nesnesini geçirerek belgeyi yükleyin, ardından belgenin içeriğini doğrulayın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
