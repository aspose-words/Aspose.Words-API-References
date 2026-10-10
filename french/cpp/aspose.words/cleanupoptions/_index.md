---
title: "Classe Aspose::Words::CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::CleanupOptions. Permet de spécifier des options pour le nettoyage du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


Permet de spécifier des options pour le nettoyage de documents. Pour en savoir plus, consultez l'article de documentation [Clean Up a Document](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | Obtient/definit un indicateur indiquant si les styles en double doivent être supprimés du document. La valeur par défaut est **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | Spécifie que les styles inutilisés [BuiltIn](../style/get_builtin/) doivent être supprimés du document. |
| [get_UnusedLists](./get_unusedlists/)() const | Spécifie si les listes inutilisées et leurs définitions doivent être supprimées du document. La valeur par défaut est **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | Spécifie si les styles inutilisés doivent être supprimés du document. La valeur par défaut est **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | Définisseur pour [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | Définisseur pour [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | Définisseur pour [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | Définisseur pour [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment supprimer tous les styles personnalisés inutilisés d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Combiné aux styles intégrés, le document possède maintenant huit styles.
// Un style personnalisé est marqué comme "utilisé" tant qu'il y a du texte dans le document
// formaté avec ce style. Cela signifie que les 4 styles que nous avons ajoutés sont actuellement inutilisés.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Appliquez un style de caractère personnalisé, puis un style de liste personnalisé. Cela les marquera comme "utilisé".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Maintenant, il y a un style de caractère inutilisé et un style de liste inutilisé.
// La méthode Cleanup(), lorsqu'elle est configurée avec un objet CleanupOptions, peut cibler les styles inutilisés et les supprimer.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Supprimer chaque nœud auquel un style personnalisé est appliqué le marque à nouveau comme "inutilisé".
// Réexécutez la méthode Cleanup pour les supprimer.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
