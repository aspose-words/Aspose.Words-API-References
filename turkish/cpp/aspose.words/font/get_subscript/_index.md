---
title: "Aspose::Words::Font::get_Subscript metodu"
linktitle: "get_Subscript"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_Subscript metodu. Yazı tipi alt simge olarak biçimlendirilmişse C++'da doğru."
type: docs
weight: 45000
url: /tr/cpp/aspose.words/font/get_subscript/
---
## Font::get_Subscript method


Yazı tipi alt simge olarak biçimlendirilmişse doğrudur.

```cpp
bool Aspose::Words::Font::get_Subscript()
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
