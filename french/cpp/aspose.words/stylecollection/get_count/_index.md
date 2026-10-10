---
title: "Aspose::Words::StyleCollection::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection::get_Count méthode. Obtient le nombre de styles dans la collection en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


Obtient le nombre de styles dans la collection.

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
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

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
