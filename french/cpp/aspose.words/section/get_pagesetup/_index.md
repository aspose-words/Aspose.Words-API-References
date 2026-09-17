---
title: "Méthode Aspose::Words::Section::get_PageSetup"
linktitle: "get_PageSetup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Section::get_PageSetup. Retourne un objet qui représente la configuration de page et les propriétés de la section en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/section/get_pagesetup/
---
## Section::get_PageSetup method


Renvoie un objet qui représente la configuration de la page et les propriétés de la section.

```cpp
System::SharedPtr<Aspose::Words::PageSetup> Aspose::Words::Section::get_PageSetup()
```


## Exemples



Montre comment créer une bordure à large bande bleue en haut de la première page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```


Montre comment construire un document Aspose.Words à la main.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et obtenez un nœud de document sans enfants.
doc->RemoveAllChildren();

// Ce document n’a maintenant aucun nœud enfant composite auquel nous puissions ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons reconstituer sa collection de nœuds.
// Tout d’abord, créez une nouvelle section, puis ajoutez-la en tant qu’enfant au nœud racine du document.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Définissez quelques propriétés de mise en page pour la section.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Une section nécessite un corps, qui contiendra et affichera tout son contenu
// sur la page entre l’en-tête et le pied-de-page de la section.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Créez un paragraphe, définissez quelques propriétés de mise en forme, puis ajoutez‑le en tant qu’enfant au corps.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Enfin, ajoutez du contenu au document. Créez un run,
// définissez son apparence et son contenu, puis ajoutez‑le en tant qu’enfant au paragraphe.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Voir aussi

* Class [PageSetup](../../pagesetup/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
