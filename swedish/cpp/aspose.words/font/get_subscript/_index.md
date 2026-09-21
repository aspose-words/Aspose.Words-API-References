---
title: "Aspose::Words::Font::get_Subscript-metod"
linktitle: "get_Subscript"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Subscript-metod. Sant om teckensnittet är formaterat som subscript i C++."
type: docs
weight: 45000
url: /sv/cpp/aspose.words/font/get_subscript/
---
## Font::get_Subscript method


Sant om teckensnittet är formaterat som nedsänkt.

```cpp
bool Aspose::Words::Font::get_Subscript()
```


## Exempel



Visar hur man formaterar text för att förskjuta dess position.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Höj denna sekvens av text 5 punkter över baslinjen.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Sänk detta textstycke 10 punkter under baslinjen.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Lägg till ett stycke normal text.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Lägg till ett textstycke som visas som nedsänkt.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Lägg till ett textstycke som visas som upphöjt.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
