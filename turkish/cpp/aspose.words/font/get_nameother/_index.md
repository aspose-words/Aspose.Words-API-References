---
title: "Aspose::Words::Font::get_NameOther metodu"
linktitle: "get_NameOther"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_NameOther metodu. C++'ta 128 ile 255 arasındaki karakter kodları için kullanılan yazı tipini döndürür veya ayarlar."
type: docs
weight: 29000
url: /tr/cpp/aspose.words/font/get_nameother/
---
## Font::get_NameOther method


128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar.

```cpp
System::String Aspose::Words::Font::get_NameOther()
```


## Örnekler



Microsoft Word'ün bir koşu içinde iki farklı yazı tipini nasıl birleştirebileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu yazı tipi yapılandırmasını kullanarak oluşturucunun eklediği bir koşuyu varsayalım.
// ASCII karakter aralığı içinde karakterler içerir. Bu durumda,
// Bu karakterleri bu yazı tipiyle gösterecektir.
builder->get_Font()->set_NameAscii(u"Calibri");

// Başka bir yazı tipi belirtilmediğinde, oluşturucu bu yazı tipini eklediği tüm karakterlere de uygular.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// ASCII aralığının dışındaki tüm karakterler için kullanılacak bir yazı tipi belirtin.
// İdeal olarak, bu yazı tipinin gerekli tüm ASCII dışı karakter kodları için bir glifi olmalıdır.
builder->get_Font()->set_NameOther(u"Courier New");

// ASCII karakterlerden oluşan bir kelime ve o aralığın dışındaki tüm karakterlerden oluşan bir kelime içeren bir koşu ekleyin.
// Her karakter, duruma bağlı olarak, bu iki yazı tipinden biriyle gösterilecektir.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
