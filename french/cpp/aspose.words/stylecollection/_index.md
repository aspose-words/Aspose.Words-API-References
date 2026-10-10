---
title: "Aspose::Words::StyleCollection classe"
linktitle: "StyleCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection classe. Une collection d'objets Style qui représentent à la fois les styles intégrés et définis par l'utilisateur dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 65000
url: /fr/cpp/aspose.words/stylecollection/
---
## StyleCollection class


Une collection d'objets [Style](../style/) qui représentent à la fois les styles intégrés et définis par l'utilisateur dans un document. Pour en savoir plus, consultez l'article de documentation [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Crée un nouveau style défini par l'utilisateur et l'ajoute à la collection. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Copie un style dans cette collection. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Supprime tous les styles du panneau Galerie Quick [Style](../style/). |
| [get_Count](./get_count/)() | Obtient le nombre de styles dans la collection. |
| [get_DefaultFont](./get_defaultfont/)() | Obtient le formatage de texte par défaut du document. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Obtient le formatage de paragraphe par défaut du document. |
| [get_Document](./get_document/)() const | Obtient le document propriétaire. |
| [GetEnumerator](./getenumerator/)() override | Obtient un objet énumérateur qui énumérera les styles par ordre alphabétique de leurs noms. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtient un style par nom ou alias. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Obtient un style intégré par son identifiant indépendant de la locale. |
| [idx_get](./idx_get/)(int32_t) | Obtient un style par index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un style de paragraphe personnalisé.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Appliquez le style de paragraphe au paragraphe actuel du constructeur de document, puis ajoutez du texte.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifiez le style du DocumentBuilder pour qu'il n'ait aucun format de liste et écrivez un autre paragraphe.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
