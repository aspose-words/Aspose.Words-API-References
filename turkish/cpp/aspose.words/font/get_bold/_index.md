---
title: "Aspose::Words::Font::get_Bold yöntemi"
linktitle: "get_Bold"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Bold yöntemi. C++'ta yazı tipi kalın olarak biçimlendirilmişse doğru."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


Yazı tipi kalın olarak biçimlendirilmişse doğru.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Örnekler



Biçimlendirilmiş metni [DocumentBuilder](../../documentbuilder/) kullanarak nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yazı tipi biçimlendirmesini belirtin, ardından metin ekleyin.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
