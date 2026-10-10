---
title: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate yöntemi"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate yöntemi. C++'da alan güncellemesi sırasında çift yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Alan güncellemesi sırasında çift yönlü metnin tam olarak desteklenip desteklenmediğini gösteren değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Açıklamalar


Bu özellik **true** olarak ayarlandığında, güncelleme sırasında sağdan sola (Right-To-Left) dilleri (ör. Arapça veya İbranice) ile uyumlu alan sonucunu üretmek için ek adımlar uygulanır.

Bu özellik **false** olarak ayarlandığında ve sağdan sola dil kullanıldığında, güncelleme sonrası alan sonucunun doğruluğu garanti edilmez.

Varsayılan değer **false**'tur.

## Örnekler



[FieldOptions](../) kullanımını gösterir ve alan güncellemesinin çift yönlü metni tam olarak desteklemesini sağlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Sağdan sola metin içeren tüm alan işlemlerinin beklendiği gibi çalıştığından emin olun.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Sağdan sola metin içeren bir alan eklemek için bir belge oluşturucu kullanın.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## Ayrıca Bakınız

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
