---
title: "Aspose::Words::Font::get_StyleIdentifier yöntemi"
linktitle: "get_StyleIdentifier"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_StyleIdentifier yöntemi. Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını alır veya ayarlar C++ içinde."
type: docs
weight: 43000
url: /tr/cpp/aspose.words/font/get_styleidentifier/
---
## Font::get_StyleIdentifier method


Bu biçimlendirmeye uygulanan karakter stilinin bölge bağımsız stil tanımlayıcısını alır veya ayarlar.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Font::get_StyleIdentifier()
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

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
