---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet méthode"
linktitle: "get_SheetsPerBooklet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet méthode. Retourne ou définit le nombre de pages à inclure dans chaque livret en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Renvoie ou définit le nombre de pages à inclure dans chaque livret.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


## Exemples



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
