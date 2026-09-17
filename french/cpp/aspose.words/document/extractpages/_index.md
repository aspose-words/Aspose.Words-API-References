---
title: "Aspose::Words::Document::ExtractPages méthode"
linktitle: "ExtractPages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::ExtractPages méthode. Retourne l'objet Document représentant la plage de pages spécifiée en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Retourne l'objet [Document](../) représentant la plage de pages spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | L'index basé sur zéro de la première page à extraire. |
| count | int32_t | Nombre de pages à extraire. |

## Exemples



Montre comment obtenir la plage de pages spécifiée du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Renvoie l'objet [Document](../) représentant la plage de pages spécifiée et les options d'extraction de page données.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | L'index basé sur zéro de la première page à extraire. |
| count | int32_t | Nombre de pages à extraire. |
| options | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Fournit des options pour gérer le processus d'extraction de pages. |

## Voir aussi

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
