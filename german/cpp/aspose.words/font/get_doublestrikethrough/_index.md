---
title: "Aspose::Words::Font::get_DoubleStrikeThrough Methode"
linktitle: "get_DoubleStrikeThrough"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_DoubleStrikeThrough Methode. True, wenn die Schriftart als doppelter Durchstrich formatiert ist, in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words/font/get_doublestrikethrough/
---
## Font::get_DoubleStrikeThrough method


True, wenn die Schrift als doppelter Durchstrich formatiert ist.

```cpp
bool Aspose::Words::Font::get_DoubleStrikeThrough()
```


## Beispiele



Zeigt, wie man einem Text einen Durchstrich hinzufügt.
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

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
