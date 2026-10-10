---
title: "Aspose::Words::Font::get_SmallCaps Methode"
linktitle: "get_SmallCaps"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_SmallCaps Methode. True, wenn die Schriftart als Kapitälchen formatiert ist in C++."
type: docs
weight: 38000
url: /de/cpp/aspose.words/font/get_smallcaps/
---
## Font::get_SmallCaps method


Wahr, wenn die Schriftart als Kapitälchen formatiert ist.

```cpp
bool Aspose::Words::Font::get_SmallCaps()
```


## Beispiele



Zeigt, wie man einen Lauf formatiert, um dessen Inhalt in Großbuchstaben anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Es gibt zwei Möglichkeiten, einen Lauf dazu zu bringen, seinen Kleinbuchtext in Großbuchstaben anzuzeigen, ohne den Inhalt zu ändern.
// 1 -  Setzen Sie das AllCaps-Flag, um alle Zeichen in regulären Großbuchstaben anzuzeigen:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  Setzen Sie das SmallCaps-Flag, um alle Zeichen in Kapitälchen anzuzeigen:
// Wenn ein Zeichen klein geschrieben ist, erscheint es in seiner Großbuchstabenform
// aber hat dieselbe Höhe wie das Kleinbuchzeichen (die x-Höhe der Schrift).
// Zeichen, die ursprünglich in Großbuchstaben waren, sehen gleich aus.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
