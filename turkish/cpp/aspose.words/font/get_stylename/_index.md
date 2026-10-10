---
title: "Aspose::Words::Font::get_StyleName yöntemi"
linktitle: "get_StyleName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_StyleName yöntemi. Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar C++'ta."
type: docs
weight: 44000
url: /tr/cpp/aspose.words/font/get_stylename/
---
## Font::get_StyleName method


Bu biçimlendirmeye uygulanan karakter stilinin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Font::get_StyleName()
```


## Örnekler



Mevcut metnin stilinin nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda stillere referans vermenin iki yolu bulunmaktadır.
// 1 -  Stil adını kullanarak:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Yerleşik bir stil tanımlayıcısını kullanarak:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Bir stilin tüm kullanımını diğerine dönüştür,
// yukarıdaki yöntemleri kullanarak eski ve yeni stillere referans vererek.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
