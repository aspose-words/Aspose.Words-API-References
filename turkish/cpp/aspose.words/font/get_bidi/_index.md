---
title: "Aspose::Words::Font::get_Bidi yöntemi"
linktitle: "get_Bidi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Bidi yöntemi. C++'ta bu çalıştırmanın içeriğinin sağdan sola özelliklere sahip olup olmadığını belirtir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir.

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## Açıklamalar


Bu özellik açık olduğunda, güçlü soldan sağa metinle kullanılmamalıdır. Bu koşul altındaki davranış belirsizdir. Bu özellik kapalı olduğunda, güçlü sağdan sola metinle kullanılmamalıdır. Bu koşul altındaki davranış belirsizdir.

Bu çalıştırmanın içeriği görüntülendiğinde, biçimlendirme amacıyla tüm karakterler karmaşık betik karakterleri olarak ele alınır. Bu, [BoldBi](../get_boldbi/), [ItalicBi](../get_italicbi/), [SizeBi](../get_sizebi/) ve ilgili bir yazı tipi adının bu çalıştırma render edildiğinde kullanılacağı anlamına gelir.

Ayrıca, bu çalıştırmanın içeriği görüntülendiğinde, bu özellik \"weak types\" ve \"neutral types\" olarak sınıflandırılan karakterler için sağdan sola geçersiz kılma işlevi görür.

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
