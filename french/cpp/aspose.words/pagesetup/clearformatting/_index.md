---
title: "Aspose::Words::PageSetup::ClearFormatting méthode"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::ClearFormatting méthode. Réinitialise la configuration de la page à la taille de papier, aux marges et à l’orientation par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/pagesetup/clearformatting/
---
## PageSetup::ClearFormatting method


Réinitialise la configuration de page à la taille de papier, aux marges et à l'orientation par défaut.

```cpp
void Aspose::Words::PageSetup::ClearFormatting()
```


## Exemples



Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifiez les propriétés de mise en page pour la section actuelle du constructeur et ajoutez du texte.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Si nous commençons une nouvelle section en utilisant un constructeur de document,
// elle héritera des propriétés de mise en page actuelles du constructeur.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Nous pouvons rétablir ses propriétés de mise en page à leurs valeurs par défaut en utilisant la méthode "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
