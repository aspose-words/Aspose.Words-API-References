---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter method"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter method. Vrai si le document possède des en-têtes et pieds de page différents pour les pages impaires et les pages paires en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Vrai si le document possède des en-têtes et pieds de page différents pour les pages impaires et paires.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Exemples



Montre comment activer ou désactiver les en-têtes/pieds de page des pages paires.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous, deux types d'en-têtes/pieds de page.
// 1 -  L'en-tête/pied de page "Principal", qui apparaît sur chaque page de la section.
// Nous pouvons remplacer l'en-tête/pied de page principal par un en-tête/pied de page de première page et un en-tête/pied de page pair.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  L'en-tête/pied de page "Pair", qui apparaît sur chaque page paire de cette section.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Chaque section possède un objet "PageSetup" qui spécifie les propriétés liées à l'apparence de la page
// telles que l'orientation, la taille et les bordures.
// Définissez la propriété "OddAndEvenPagesHeaderFooter" sur "true"
// pour afficher l'en-tête/pied de page des pages paires sur les pages paires.
// Définissez la propriété "OddAndEvenPagesHeaderFooter" sur "false"
// pour afficher l'en-tête/pied de page principal sur les pages paires.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
