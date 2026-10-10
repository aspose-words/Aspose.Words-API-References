---
title: "Aspose::Words::Font::get_StrikeThrough metodu"
linktitle: "get_StrikeThrough"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_StrikeThrough metodu. C++'da font üstü çizili metin olarak biçimlendirilmişse doğru."
type: docs
weight: 41000
url: /tr/cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


Yazı tipi üzeri çizili metin olarak biçimlendirilmişse doğrudur.

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
```


## Örnekler



Metne bir satır üstü çizgi eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.StrikeThrough.docx");
```

## Ayrıca Bakınız

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
