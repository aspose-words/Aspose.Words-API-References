---
title: "Aspose::Words::Font::get_StrikeThrough metod"
linktitle: "get_StrikeThrough"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_StrikeThrough metod. Sant om teckensnittet är formaterat som genomstruken text i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


Sant om teckensnittet är formaterat som genomstruken text.

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
```


## Exempel



Visar hur man lägger till en genomstruken linje i text.
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

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
