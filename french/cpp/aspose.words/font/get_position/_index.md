---
title: "Méthode Aspose::Words::Font::get_Position"
linktitle: "get_Position"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Font::get_Position. Obtient ou définit la position du texte (en points) par rapport à la ligne de base. Un nombre positif élève le texte, et un nombre négatif l'abaisse en C++."
type: docs
weight: 32000
url: /fr/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


Obtient ou définit la position du texte (en points) par rapport à la ligne de base. Un nombre positif élève le texte, et un nombre négatif l'abaisse.

```cpp
double Aspose::Words::Font::get_Position()
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
