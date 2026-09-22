---
title: "Aspose::Words::ParagraphFormat::get_RightIndent metodu"
linktitle: "get_RightIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_RightIndent metodu. C++'ta paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) alır veya ayarlar."
type: docs
weight: 28000
url: /tr/cpp/aspose.words/paragraphformat/get_rightindent/
---
## ParagraphFormat::get_RightIndent method


Paragraf için sağ girintiyi temsil eden değeri (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::ParagraphFormat::get_RightIndent()
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
