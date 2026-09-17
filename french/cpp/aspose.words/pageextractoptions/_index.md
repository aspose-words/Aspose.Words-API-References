---
title: "Classe Aspose::Words::PageExtractOptions"
linktitle: "PageExtractOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::PageExtractOptions. Permet de spécifier des options pour l'extraction de pages de document en C++."
type: docs
weight: 45500
url: /fr/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


Permet de spécifier des options pour l'extraction de pages de document.

```cpp
class PageExtractOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | Spécifie si les champs NUMPAGES dans le document résultant seront remplacés par leurs valeurs réelles. La valeur par défaut est **true**. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | Spécifie si le numéro de page de départ dans le document résultant doit être mis à jour. La valeur par défaut est **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | Mutateur pour [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | Mutateur pour [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

## Exemples



Montrez comment réinitialiser la numérotation de page initiale et enregistrer le champ NUMPAGE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Comportement par défaut :
// La numérotation des pages extraites est la même que dans le document original, comme si nous avions sélectionné "Print 2 pages" dans MS Word.
// La page de départ sera définie à 2 et le champ indiquant le nombre de pages sera supprimé
// et remplacé par une valeur constante égale au nombre de pages.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Comportement modifié :
// La numérotation des pages extraites est réinitialisée et une nouvelle commence,
// comme si nous avions copié le contenu de la deuxième page et l'avions collé dans un nouveau document.
// La page de départ sera définie à 1 et le champ indiquant le nombre de pages restera inchangé
// et affichera le nombre actuel de pages.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
