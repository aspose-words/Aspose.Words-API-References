---
title: "Aspose::Words::Font::get_AllCaps yöntemi"
linktitle: "get_AllCaps"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_AllCaps metodu. C++'ta yazı tipi tüm büyük harflerle biçimlendirilmişse doğru."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/font/get_allcaps/
---
## Font::get_AllCaps method


Yazı tipi tüm büyük harflerle biçimlendirilmişse doğru.

```cpp
bool Aspose::Words::Font::get_AllCaps()
```


## Örnekler



Bir run'un içeriğini büyük harflerle gösterecek şekilde nasıl biçimlendireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// İçeriği değiştirmeden bir run'un küçük harfli metnini büyük harfe dönüştürmenin iki yolu vardır.
// 1 -  AllCaps bayrağını ayarlayarak tüm karakterleri normal büyük harflerle gösterin:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  SmallCaps bayrağını ayarlayarak tüm karakterleri küçük büyük harflerle gösterin:
// Bir karakter küçük harf ise, büyük harf biçiminde görünecektir
// ancak yüksekliği küçük harf (yazı tipinin x-yüksekliği) ile aynı olacaktır.
// Başlangıçta büyük harf olan karakterler aynı görünecektir.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
