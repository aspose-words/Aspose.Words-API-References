---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphAlignment enum. Spécifie l'alignement du texte dans un paragraphe en C++."
type: docs
weight: 110000
url: /fr/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Spécifie l'alignement du texte dans un paragraphe.

```cpp
enum class ParagraphAlignment
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Gauche | 0 | Le texte est aligné à gauche. |
| Centre | 1 | Le texte est centré horizontalement. |
| Droite | 2 | Le texte est aligné à droite. |
| Justifier | 3 | Le texte est aligné à gauche et à droite. |
| Distribué | 4 | Le texte est réparti uniformément. |
| ArabicMediumKashida | 5 | Arabe uniquement. La longueur du Kashida pour le texte est étendue à une longueur moyenne déterminée par le consommateur. |
| ArabicHighKashida | 7 | Arabe uniquement. La longueur du Kashida pour le texte est étendue à sa longueur maximale possible. |
| ArabicLowKashida | 8 | Arabe uniquement. La longueur du Kashida pour le texte est étendue à une longueur légèrement plus longue. |
| ThaiDistributed | 9 | Thaï uniquement. Le texte est justifié avec une optimisation pour le thaï. |
| MathElementCenterAsGroup | 10 | Le seul élément [Math](../../aspose.words.math/) dans une ligne, aligné comme 'Centré en groupe'. |


## Exemples



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
