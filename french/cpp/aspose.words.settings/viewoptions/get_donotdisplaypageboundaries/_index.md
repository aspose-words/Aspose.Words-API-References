---
title: "Méthode get_DoNotDisplayPageBoundaries de Aspose::Words::Settings::ViewOptions"
linktitle: "get_DoNotDisplayPageBoundaries"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode get_DoNotDisplayPageBoundaries de Aspose::Words::Settings::ViewOptions. Désactive l'affichage de l'espace entre le haut du texte et le bord supérieur de la page en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.settings/viewoptions/get_donotdisplaypageboundaries/
---
## ViewOptions::get_DoNotDisplayPageBoundaries method


Désactive l'affichage de l'espace entre le haut du texte et le bord supérieur de la page.

```cpp
bool Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries() const
```


## Exemples



Montre comment masquer les espaces blancs verticaux et les en-têtes/pieds de page dans les options d'affichage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez du contenu qui s'étend sur 3 pages.
builder->Writeln(u"Paragraph 1, Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 2, Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Paragraph 3, Page 3.");

// Insérez un en-tête et un pied de page.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the footer.");

// Ce document contient une petite quantité de contenu qui occupe l'équivalent de quelques pages complètes.
// Définissez le drapeau "DoNotDisplayPageBoundaries" sur "true" pour que les anciennes versions de Microsoft Word omettent les en-têtes,
// les pieds de page et la plupart des espaces blancs verticaux lors de l'affichage de notre document.
// Définissez le drapeau "DoNotDisplayPageBoundaries" sur "false" pour que les anciennes versions de Microsoft Word
// affichent normalement notre document.
doc->get_ViewOptions()->set_DoNotDisplayPageBoundaries(doNotDisplayPageBoundaries);

doc->Save(get_ArtifactsDir() + u"ViewOptions.DisplayPageBoundaries.doc");
```

## Voir aussi

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
