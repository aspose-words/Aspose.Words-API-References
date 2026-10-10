---
title: "Aspose::Words::Font::get_SizeBi yöntemi"
linktitle: "get_SizeBi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_SizeBi yöntemi. C++'da sağdan sola belge içinde kullanılan yazı tipi boyutunu nokta cinsinden alır veya ayarlar."
type: docs
weight: 37000
url: /tr/cpp/aspose.words/font/get_sizebi/
---
## Font::get_SizeBi method


Sağdan sola belge içinde kullanılan yazı tipi boyutunu puan cinsinden alır veya ayarlar.

```cpp
double Aspose::Words::Font::get_SizeBi()
```


## Örnekler



Sağdan sola ve sağdan sola metin için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Soldan sağa metin için bir yazı tipi ayarları kümesi tanımlayın.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Sağdan sola metin için başka bir yazı tipi ayarları kümesi tanımlayın.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// Bidi bayrağını, ekleyeceğimiz metnin sağdan sola olup olmadığını göstermek için kullanabiliriz.
// belge oluşturucu ile sağdan sola olduğunu gösterir. Bu bayrak true olarak ayarlandığında metin eklediğimizde,
// sağdan sola yazı tipi ayarları kümesi kullanılarak biçimlendirilir.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Bayrağı false olarak ayarlayın ve ardından soldan sağa metin ekleyin.
// Belge oluşturucu, bunları soldan sağa yazı tipi ayarları kümesiyle biçimlendirecektir.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
