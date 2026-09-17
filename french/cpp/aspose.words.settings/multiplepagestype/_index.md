---
title: "Énumération Aspose::Words::Settings::MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Énumération Aspose::Words::Settings::MultiplePagesType. Spécifie comment le document est imprimé en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Spécifie comment le document est imprimé.

```cpp
enum class MultiplePagesType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Normal | 0 | Impression normale, aucune page multiple spécifiée. |
| MirrorMargins | 1 | Échange les marges gauche et droite sur les pages en vis-à-vis. |
| TwoPagesPerSheet | 2 | Imprime deux pages par feuille. |
| BookFoldPrinting | 3 | Spécifie s’il faut imprimer le document sous forme de pliage de livre. |
| BookFoldPrintingReverse | 4 | Spécifie s’il faut imprimer le document sous forme de pliage de livre inversé. |
| Default | n/a | La valeur par défaut est [Normal](./) |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
