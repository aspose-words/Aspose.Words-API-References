---
title: "Aspose::Words::PaperSize enum"
linktitle: "PaperSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PaperSize enum. Spécifie la taille du papier en C++."
type: docs
weight: 109000
url: /fr/cpp/aspose.words/papersize/
---
## PaperSize enum


Spécifie la taille du papier.

```cpp
enum class PaperSize
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| A3 | 0 | 297 x 420 mm. |
| A4 | 1 | 210 x 297 mm. |
| A5 | 2 | 148 x 210 mm. |
| B4 | 3 | 250 x 353 mm. |
| B5 | 4 | 176 x 250 mm. |
| Exécutif | 5 | 7,25 x 10,5 pouces. |
| Folio | 6 | 8,5 x 13 pouces. |
| Ledger | 7 | 17 x 11 pouces. |
| Légal | 8 | 8,5 x 14 pouces. |
| Lettre | 9 | 8,5 x 11 pouces. |
| EnvelopeDL | 10 | 110 x 220 mm. |
| Quarto | 11 | 8,47 x 10,83 pouces. |
| Déclaration | 12 | 8,5 x 5,5 pouces. |
| Tabloïd | 13 | 11 x 17 pouces. |
| Paper10x14 | 14 | 10 x 14 pouces. |
| Paper11x17 | 15 | 11 x 17 pouces. |
| Number10Envelope | 16 | 4,125 x 9,5 pouces. |
| JisB4 | 17 | 257 x 364 mm. |
| JisB5 | 18 | 182 x 257 mm. |
| Personnalisé | 19 | Taille de papier personnalisée. |


## Exemples



Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Montre comment définir les tailles de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nous pouvons changer la taille de la page actuelle en une taille prédéfinie
// en utilisant la propriété "PaperSize" de l'objet PageSetup de cette section.
builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Tabloid);

ASPOSE_ASSERT_EQ(792.0, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(1224.0, builder->get_PageSetup()->get_PageHeight());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

// Chaque section possède son propre objet PageSetup. Lorsque nous utilisons un constructeur de document pour créer une nouvelle section,
// l'objet PageSetup de cette section hérite de toutes les valeurs de l'objet PageSetup de la section précédente.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

ASSERT_EQ(Aspose::Words::PaperSize::Tabloid, builder->get_PageSetup()->get_PaperSize());

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::A5);
builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

ASPOSE_ASSERT_EQ(419.55, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(595.30, builder->get_PageSetup()->get_PageHeight());

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

// Définissez une taille personnalisée pour les pages de cette section.
builder->get_PageSetup()->set_PageWidth(620);
builder->get_PageSetup()->set_PageHeight(480);

ASSERT_EQ(Aspose::Words::PaperSize::Custom, builder->get_PageSetup()->get_PaperSize());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

doc->Save(get_ArtifactsDir() + u"PageSetup.PaperSizes.docx");
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
