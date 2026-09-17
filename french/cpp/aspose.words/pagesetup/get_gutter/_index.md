---
title: "Aspose::Words::PageSetup::get_Gutter méthode"
linktitle: "get_Gutter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_Gutter méthode. Obtient ou définit la quantité d'espace supplémentaire ajoutée à la marge pour la reliure du document en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words/pagesetup/get_gutter/
---
## PageSetup::get_Gutter method


Obtient ou définit la quantité d’espace supplémentaire ajoutée à la marge pour la reliure du document.

```cpp
double Aspose::Words::PageSetup::get_Gutter()
```


## Exemples



Montre comment définir les marges de gouttière.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez du texte qui s’étend sur plusieurs pages.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Une gouttière ajoute des espaces blancs à la marge gauche ou droite de la page,
// ce qui compense le pliage central des pages d’un livre empiétant sur la mise en page de la page.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Déterminez l’espace disponible pour le texte à l’intérieur des marges de nos pages, puis ajoutez une valeur pour élargir une marge.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Définissez la propriété "RtlGutter" sur "true" pour placer la gouttière à une position plus adaptée au texte de droite à gauche.
pageSetup->set_RtlGutter(true);

// Définissez la propriété "MultiplePages" sur "MultiplePagesType.MirrorMargins" pour alterner
// la position des marges côté gauche/droite à chaque page.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```


Montre comment configurer un document qui peut être imprimé sous forme de pliage de livre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insérez du texte qui s’étend sur 16 pages.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Configurez la propriété "PageSetup" de la première section pour imprimer le document sous forme de pliage de livre.
// Lorsque nous imprimons ce document des deux côtés, nous pouvons prendre les pages pour les empiler
// et les plier toutes en même temps au centre. Le contenu du document s’alignera en un pliage de livre.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Nous ne pouvons spécifier le nombre de feuilles qu'en multiples de 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
