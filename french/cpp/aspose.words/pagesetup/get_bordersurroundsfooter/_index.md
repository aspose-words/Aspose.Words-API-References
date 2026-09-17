---
title: "Méthode Aspose::Words::PageSetup::get_BorderSurroundsFooter"
linktitle: "get_BorderSurroundsFooter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PageSetup::get_BorderSurroundsFooter. Indique si la bordure de la page inclut ou exclut le pied de page en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/pagesetup/get_bordersurroundsfooter/
---
## PageSetup::get_BorderSurroundsFooter method


Spécifie si la bordure de page inclut ou exclut le pied de page.

```cpp
bool Aspose::Words::PageSetup::get_BorderSurroundsFooter()
```


## Exemples



Montre comment appliquer une bordure à la page et à l’en-tête/pied de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This is the main body text.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer.");
builder->MoveToDocumentEnd();

// Insérez une bordure bleue à double ligne.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// L'objet PageSetup d'une section possède les indicateurs "BorderSurroundsHeader" et "BorderSurroundsFooter" qui déterminent
// si une bordure de page entoure le texte principal du corps, inclut également l'en-tête ou le pied de page, respectivement.
// Définissez l'indicateur "BorderSurroundsHeader" sur "true" pour entourer l'en-tête avec notre bordure,
// et définissez ensuite l'indicateur "BorderSurroundsFooter" pour laisser le pied de page à l'extérieur de la bordure.
pageSetup->set_BorderSurroundsHeader(true);
pageSetup->set_BorderSurroundsFooter(false);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorder.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
