---
title: "Aspose::Words::Font::get_Position yöntemi"
linktitle: "get_Position"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Position yöntemi. Metnin konumunu (nokta cinsinden) temel çizgiye göre alır veya ayarlar. Pozitif bir sayı metni yükseltir, negatif bir sayı ise alçaltır C++'de."
type: docs
weight: 32000
url: /tr/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


Metnin (puan cinsinden) temel çizgiye göre konumunu alır veya ayarlar. Pozitif bir sayı metni yükseltir, negatif bir sayı ise alçaltır.

```cpp
double Aspose::Words::Font::get_Position()
```


## Örnekler



Metnin konumunu kaydırmak için nasıl biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Bu metin yürütmesini temel çizginin 5 nokta üzerisine yükseltin.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Bu metin yürütmesini temel çizginin 10 nokta altına indirin.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Normal bir metin yürütmesi ekleyin.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Alt simge olarak görünecek bir metin yürütmesi ekleyin.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Üst simge olarak görünecek bir metin yürütmesi ekleyin.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
