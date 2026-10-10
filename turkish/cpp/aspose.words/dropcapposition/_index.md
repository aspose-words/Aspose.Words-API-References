---
title: "Aspose::Words::DropCapPosition enum"
linktitle: "DropCapPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DropCapPosition enum. C++'da bir drop cap metni için konumu belirtir."
type: docs
weight: 87000
url: /tr/cpp/aspose.words/dropcapposition/
---
## DropCapPosition enum


Bir drop cap metni için konumu belirtir.

```cpp
enum class DropCapPosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Paragrafta drop cap bulunmuyor. |
| Normal | 1 | Drop cap, referans paragrafta metin kenar boşluğunun içinde konumlandırılmıştır. |
| Kenar boşluğu | 2 | Drop cap, referans paragrafta metin kenar boşluğunun dışında konumlandırılmıştır. |


## Örnekler



Bir drop cap nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// İkinci ve üçüncü paragrafların metniyle başlayan büyük bir harfle bir paragraf ekleyin.
builder->get_Font()->set_Size(54);
builder->Writeln(u"L");

builder->get_Font()->set_Size(18);
builder->Writeln(System::String(u"orem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder->Writeln(System::String(u"Ut enim ad minim veniam, quis nostrud exercitation ") + u"ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Şu anda, ikinci ve üçüncü paragraflar birincinin altında görünecek.
// İlk paragrafı, diğer paragraflar için bir drop cap olarak, "ParagraphFormat" nesnesi aracılığıyla dönüştürebiliriz.
// Drop cap'i yerleştirmek için "DropCapPosition" özelliğini "DropCapPosition.Margin" olarak ayarlayın
// metnimiz soldan sağa ise sayfanın sol kenar boşluğunun dışına.
// Drop cap'i sayfa kenar boşlukları içinde yerleştirmek için "DropCapPosition" özelliğini "DropCapPosition.Normal" olarak ayarlayın
// ve metnin geri kalanını onun etrafına saracak şekilde.
// "DropCapPosition.None" tüm paragraflar için varsayılan durumdur.
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_DropCapPosition(dropCapPosition);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.DropCap.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
