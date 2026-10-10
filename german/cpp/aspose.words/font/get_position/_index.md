---
title: "Aspose::Words::Font::get_Position Methode"
linktitle: "get_Position"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Position Methode. Gibt die Position des Textes (in Punkten) relativ zur Grundlinie zurück oder setzt sie. Eine positive Zahl hebt den Text an, und eine negative Zahl senkt ihn in C++."
type: docs
weight: 32000
url: /de/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


Liest oder legt die Position des Textes (in Punkten) relativ zur Grundlinie fest. Eine positive Zahl hebt den Text an, und eine negative Zahl senkt ihn.

```cpp
double Aspose::Words::Font::get_Position()
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
