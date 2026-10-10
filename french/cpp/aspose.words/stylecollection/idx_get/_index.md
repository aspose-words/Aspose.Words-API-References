---
title: "Aspose::Words::StyleCollection::idx_get méthode"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection::idx_get méthode. Obtient un style intégré par son identifiant indépendant de la langue en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Obtient un style intégré par son identifiant indépendant de la locale.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Une valeur [StyleIdentifier](../../styleidentifier/) qui spécifie le style intégré à récupérer. |
## Remarques


Lors de l’accès à un style qui n’existe pas encore, il est créé automatiquement.

## Exemples



Montre comment ajouter un [Style](../../style/) à la collection de styles d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si nous ajoutons un style de "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété "DefaultParagraphFormat" à la propriété "ParagraphFormat" du style.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Ajoutez un style, puis vérifiez qu’il possède les paramètres par défaut.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Voir aussi

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Obtient un style par nom ou alias.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Remarques


Sensible à la casse, renvoie **null** si le style avec le nom donné n’est pas trouvé.

Si c’est un nom anglais d’un style intégré qui n’existe pas encore, il est créé automatiquement.

## Exemples



Indique quand recalculer la mise en page du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Enregistrer un document au format PDF, en image, ou l'imprimer pour la première fois déclenchera automatiquement
// mise en cache de la mise en page du document dans ses pages.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifiez le document d'une certaine manière.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Dans la version actuelle d'Aspose.Words, la modification du document ne reconstruit pas automatiquement
// la mise en page mise en cache. Si nous souhaitons que la mise en cache
// pour rester à jour, nous devrons la mettre à jour manuellement.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Voir aussi

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Obtient un style par index.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Exemples



Montre comment ajouter un [Style](../../style/) à la collection de styles d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si nous ajoutons un style de "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété "DefaultParagraphFormat" à la propriété "ParagraphFormat" du style.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Ajoutez un style, puis vérifiez qu’il possède les paramètres par défaut.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Voir aussi

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
