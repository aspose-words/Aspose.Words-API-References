---
title: "Aspose::Words::Font::get_Outline metodu"
linktitle: "get_Outline"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Outline metodu. C++'da font anahat olarak biçimlendirilmişse doğru."
type: docs
weight: 31000
url: /tr/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


Yazı tipi taslak olarak biçimlendirilmişse doğrudur.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Örnekler



Anahat olarak biçimlendirilmiş bir metin akışı oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Metnin dolgu rengini beyaza değiştirmek için Outline bayrağını ayarlayın ve
// Metnin orijinal renginde her karakterin etrafında ince bir anahat bırakır.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
