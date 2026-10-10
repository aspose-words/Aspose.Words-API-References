---
title: "Aspose::Words::Font::get_SmallCaps méthode"
linktitle: "get_SmallCaps"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_SmallCaps méthode. Vrai si la police est formatée en petites majuscules en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words/font/get_smallcaps/
---
## Font::get_SmallCaps method


Vrai si la police est formatée en petites majuscules.

```cpp
bool Aspose::Words::Font::get_SmallCaps()
```


## Exemples



Montre comment formater un segment pour afficher son contenu en majuscules.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Il existe deux manières de faire afficher un segment son texte en minuscules en majuscules sans modifier le contenu.
// 1 -  Définissez le drapeau AllCaps pour afficher tous les caractères en majuscules normales :
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  Définissez le drapeau SmallCaps pour afficher tous les caractères en petites majuscules :
// Si un caractère est en minuscule, il apparaîtra sous forme de majuscule
// mais aura la même hauteur que la minuscule (la hauteur x de la police).
// Les caractères qui étaient déjà en majuscules resteront identiques.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
