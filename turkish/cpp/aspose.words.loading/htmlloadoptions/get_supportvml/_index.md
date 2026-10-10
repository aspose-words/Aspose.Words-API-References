---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml yöntemi"
linktitle: "get_SupportVml"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml yöntemi. C++'de VML görüntülerinin desteklenip desteklenmeyeceğini belirten bir değeri alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.loading/htmlloadoptions/get_supportvml/
---
## HtmlLoadOptions::get_SupportVml method


VML görsellerini destekleyip desteklemeyeceğini belirten bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml() const
```


## Örnekler



HTML belgesi yüklenirken koşullu yorumları nasıl destekleyeceğinizi gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Değer doğru ise, yüklü belgeyi ayrıştırırken VML kodunu dikkate alırız.
loadOptions->set_SupportVml(supportVml);

// Bu belge, "<!--[if gte vml 1]>" etiketleri içinde bir JPEG görüntüsü içerir,
// ve "<![if !vml]>" etiketleri içinde farklı bir PNG görüntüsü içerir.
// Eğer "SupportVml" bayrağını "true" olarak ayarlarsak, Aspose.Words JPEG'i yükleyecektir.
// Bu bayrağı "false" olarak ayarlarsak, Aspose.Words sadece PNG'yi yükleyecektir.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## Ayrıca Bakınız

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
