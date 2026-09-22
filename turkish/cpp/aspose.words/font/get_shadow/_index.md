---
title: "Aspose::Words::Font::get_Shadow yöntemi"
linktitle: "get_Shadow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Shadow yöntemi. Font C++ içinde gölgeli olarak biçimlendirilmişse doğru."
type: docs
weight: 35000
url: /tr/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


Yazı tipi gölgeli olarak biçimlendirilmişse doğrudur.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Örnekler



Gölgeli biçimlendirilmiş bir metin akışı oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gölgeli efekti uygulamak için Shadow bayrağını ayarlayın,
// harflerin sayfanın üzerinde süzülüyormuş gibi görünmesini sağlar.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
