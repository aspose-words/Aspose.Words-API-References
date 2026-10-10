---
title: "Aspose::Words::Font::get_Italic yöntemi"
linktitle: "get_Italic"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Italic yöntemi. Yazı tipi C++'de italik olarak biçimlendirilmişse doğru."
type: docs
weight: 18000
url: /tr/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


Yazı tipi italik olarak biçimlendirilmişse Doğru.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Örnekler



Bir belge oluşturucu kullanarak italik metin nasıl yazılır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
