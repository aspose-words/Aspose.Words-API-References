---
title: "Aspose::Words::Font::get_Subscript-Methode"
linktitle: "get_Subscript"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Subscript-Methode. Wahr, wenn die Schriftart in C++ als Tiefstellung formatiert ist."
type: docs
weight: 45000
url: /de/cpp/aspose.words/font/get_subscript/
---
## Font::get_Subscript method


Wahr, wenn die Schriftart als Tiefstellung formatiert ist.

```cpp
bool Aspose::Words::Font::get_Subscript()
```


## Beispiele



Zeigt, wie man Text formatiert, um seine Position zu verschieben.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Erhöhen Sie diesen Textlauf um 5 Punkte über die Grundlinie.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Senken Sie diesen Textlauf um 10 Punkte unter die Grundlinie.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Fügen Sie einen Lauf normalen Textes hinzu.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Fügen Sie einen Lauf Text hinzu, der als Tiefstellung angezeigt wird.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Fügen Sie einen Lauf Text hinzu, der als Hochstellung angezeigt wird.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
