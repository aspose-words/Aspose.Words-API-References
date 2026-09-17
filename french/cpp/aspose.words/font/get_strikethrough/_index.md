---
title: "Aspose::Words::Font::get_StrikeThrough méthode"
linktitle: "get_StrikeThrough"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_StrikeThrough méthode. Vrai si la police est formatée en texte barré en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


Vrai si la police est formatée avec du texte barré.

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
```


## Exemples



Montre comment ajouter un texte barré d'une ligne.
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

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
