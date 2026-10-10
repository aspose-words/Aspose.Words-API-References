---
title: "Aspose::Words::Font::get_Hidden yöntemi"
linktitle: "get_Hidden"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Hidden yöntemi. C++'ta yazı tipi gizli metin olarak biçimlendirilmişse doğru (true) döner."
type: docs
weight: 16000
url: /tr/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


Yazı tipi gizli metin olarak biçimlendirilmişse doğru.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Örnekler



Gizli metin oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gizli bayrağı true olarak ayarlandığında, bu Font nesnesiyle oluşturduğumuz tüm metin belgede görünmez olacaktır.
// Gizli metin seçeneğini etkinleştirmediğimiz sürece gizli metni göremez veya vurgulayamayız
// \"Dosya\" -> \"Seçenekler\" -> \"Görüntüleme\" yoluyla Microsoft Word'de bulunur. Metin hâlâ orada kalacaktır,
// ve bu metne programlı olarak erişebileceğiz.
// Bu yöntemi hassas bilgileri gizlemek için kullanmanız önerilmez.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
