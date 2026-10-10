---
title: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter méthode"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter méthode. Vrai si un en-tête ou pied de page différent est utilisé sur la première page en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


Vrai si un en-tête ou pied de page différent est utilisé sur la première page.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Exemples



Montre comment activer ou désactiver les en-têtes/pieds de page principaux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous, deux types d'en-têtes/pieds de page.
// 1 -  L"First" en-tête/pied de page, qui apparaît sur la première page de la section.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  L"Primary" en-tête/pied de page, qui apparaît sur chaque page de la section.
// Nous pouvons remplacer l'en-tête/pied de page principal par un en-tête/pied de page de première page et un en-tête/pied de page pair.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Chaque section possède un objet "PageSetup" qui spécifie les propriétés liées à l'apparence de la page
// telles que l'orientation, la taille et les bordures.
// Définissez la propriété "DifferentFirstPageHeaderFooter" sur "true" pour appliquer le premier en-tête/pied de page à la première page.
// Définissez la propriété "DifferentFirstPageHeaderFooter" sur "false"
// pour que la première page affiche l'en-tête/pied de page principal.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
