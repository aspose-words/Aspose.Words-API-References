---
title: "Aspose::Words::ParagraphFormat::get_LeftIndent method"
linktitle: "get_LeftIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_LeftIndent yöntemi. Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) alır veya ayarlar (C++)."
type: docs
weight: 19000
url: /tr/cpp/aspose.words/paragraphformat/get_leftindent/
---
## ParagraphFormat::get_LeftIndent method


Paragraf için sol girintiyi temsil eden değeri (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::ParagraphFormat::get_LeftIndent()
```


## Örnekler



Metni merkezin dışına yerleştirmek için paragraf biçimlendirmesinin nasıl yapılandırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belge oluşturucunun yazdığı tüm metni ortalayın ve girintileri ayarlayın.
// Aşağıdaki girinti yapılandırması, sayfada asimetrik bir şekilde konumlanacak bir metin bloğu oluşturacaktır.
// Metni hizaladığımız "merkez", metin gövdesinin ortası olacak, sayfanın ortası değil.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
