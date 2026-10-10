---
title: "Méthode Aspose::Words::PageSetup::get_Bidi"
linktitle: "get_Bidi"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PageSetup::get_Bidi. Spécifie que cette section contient du texte bidirectionnel (scripts complexes) en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Spécifie que cette section contient du texte bidirectionnel (scripts complexes).

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Remarques


Lorsque **true**, les colonnes de cette section sont disposées de droite à gauche.

## Exemples



Montre comment définir l’ordre des colonnes de texte dans une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Définissez la propriété "Bidi" sur "true" pour disposer les colonnes en commençant du côté droit de la page.
// L’ordre des colonnes correspondra à la direction du texte de droite à gauche.
// Définissez la propriété "Bidi" sur "false" pour disposer les colonnes en commençant du côté gauche de la page.
// L’ordre des colonnes correspondra à la direction du texte de gauche à droite.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
