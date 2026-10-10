---
title: "Aspose::Words::Font::get_BoldBi metodu"
linktitle: "get_BoldBi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_BoldBi metodu. C++'ta sağdan sola metin kalın olarak biçimlendirilmişse doğru."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/font/get_boldbi/
---
## Font::get_BoldBi method


Sağdan sola metin kalın olarak biçimlendirilmişse doğru.

```cpp
bool Aspose::Words::Font::get_BoldBi()
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
