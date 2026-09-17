---
title: "Méthode Aspose::Words::Document::Cleanup"
linktitle: "Cleanup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::Cleanup. Nettoie les styles et listes inutilisés du document en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/document/cleanup/
---
## Document::Cleanup() method


Nettoie les styles et listes inutilisés du document.

```cpp
void Aspose::Words::Document::Cleanup()
```


## Exemples



Montre comment supprimer les styles personnalisés inutilisés d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Combiné aux styles intégrés, le document possède maintenant huit styles.
// Un style personnalisé est considéré comme « utilisé » lorsqu'il est appliqué à une partie du document,
// ce qui signifie que les quatre styles que nous avons ajoutés sont actuellement inutilisés.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Appliquez un style de caractère personnalisé, puis un style de liste personnalisé. Cela marquera les styles comme « utilisés ».
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

doc->Cleanup();

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Supprimer chaque nœud auquel un style personnalisé est appliqué le marque à nouveau comme "inutilisé".
// Exécutez à nouveau la méthode Cleanup pour les supprimer.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup();

ASSERT_EQ(4, doc->get_Styles()->get_Count());
```

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Cleanup(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) method


Nettoie les styles et listes inutilisés du document en fonction des [CleanupOptions](../../cleanupoptions/) fournis.

```cpp
void Aspose::Words::Document::Cleanup(const System::SharedPtr<Aspose::Words::CleanupOptions> &options)
```


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

* Class [CleanupOptions](../../cleanupoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
