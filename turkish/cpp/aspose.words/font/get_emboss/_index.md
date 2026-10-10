---
title: "Aspose::Words::Font::get_Emboss yöntemi"
linktitle: "get_Emboss"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Emboss yöntemi. Font C++'ta kabartmalı olarak biçimlendirilmişse doğru."
type: docs
weight: 12000
url: /tr/cpp/aspose.words/font/get_emboss/
---
## Font::get_Emboss method


Yazı tipi kabartmalı olarak biçimlendirilmişse doğru.

```cpp
bool Aspose::Words::Font::get_Emboss()
```


## Örnekler



Metne gravür/kabartma etkileri uygulamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Aşağıda, metne 3D benzeri bir etki vermek için gölgeler kullanmanın iki yolu verilmiştir.
// 1 -  Harflerin sayfaya gömülmüş gibi görünmesi için metni gravürleyin:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Harflerin sayfadan dışarı çıkıyormuş gibi görünmesi için metni kabartın:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
