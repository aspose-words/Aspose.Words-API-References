---
title: "Aspose::Words::PageSetup::get_PageNumberStyle méthode"
linktitle: "get_PageNumberStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_PageNumberStyle méthode. Obtient ou définit le format du numéro de page en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words/pagesetup/get_pagenumberstyle/
---
## PageSetup::get_PageNumberStyle method


Obtient ou définit le format du numéro de page.

```cpp
Aspose::Words::NumberStyle Aspose::Words::PageSetup::get_PageNumberStyle()
```


## Exemples



Montre comment configurer la numérotation des pages dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 1, page 3.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Writeln(u"Section 2, page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Section 2, page 3.");

// Déplacez le constructeur de document vers l'en-tête principal de la première section,
// qui sera affiché sur chaque page de cette section.
builder->MoveToSection(0);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);

// Insérez un champ PAGE, qui affichera le numéro de la page actuelle.
builder->Write(u"Page ");
builder->InsertField(u"PAGE", u"");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 5.
// De plus, configurez tous les champs PAGE pour afficher leurs numéros de page en chiffres romains majuscules.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageStartingNumber(5);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);

// Créez un autre en-tête principal pour la deuxième section, avec un autre champ PAGE.
builder->MoveToSection(1);
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u" - ");
builder->InsertField(u"PAGE", u"");
builder->Write(u" - ");

// Configurez la section pour que le nombre de pages affiché par les champs PAGE commence à 10.
// De plus, configurez tous les champs PAGE pour afficher leurs numéros de page en chiffres arabes.
pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
pageSetup->set_PageStartingNumber(10);
pageSetup->set_RestartPageNumbering(true);
pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::Arabic);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageNumbering.docx");
```

## Voir aussi

* Enum [NumberStyle](../../numberstyle/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
