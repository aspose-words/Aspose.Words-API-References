---
title: "Aspose::Words::Font::get_Superscript méthode"
linktitle: "get_Superscript"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_Superscript méthode. Vrai si la police est formatée en exposant en C++."
type: docs
weight: 46000
url: /fr/cpp/aspose.words/font/get_superscript/
---
## Font::get_Superscript method


Vrai si la police est formatée en exposant.

```cpp
bool Aspose::Words::Font::get_Superscript()
```


## Exemples



Montre comment formater le texte pour décaler sa position.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Élevez ce segment de texte de 5 points au-dessus de la ligne de base.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Abaissez ce segment de texte de 10 points en dessous de la ligne de base.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Ajoutez un segment de texte normal.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Ajoutez un segment de texte qui apparaît en indice.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Ajoutez un segment de texte qui apparaît en exposant.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
